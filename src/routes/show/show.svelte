<script lang="ts">
    import { onMount } from "svelte";
    import {empl} from "./empStore";

  
    export let emp = [];
  
    let prefix = "";

    export let selectedEmployee;

    $: filteredemp = prefix
      ? emp.filter((e) => {
          const name = `${e.name}`;
  
          return name.toLowerCase().startsWith(prefix.toLowerCase());
        })
      : emp;
  
    // $: reset_inputs(selected);
  
    onMount(async () => {
      try {
        const response = await fetch("http://localhost:3000/emp");
        const data = await response.json();
        // console.log(data); // Check the structure of the response
        emp = Array.isArray(data) ? data : [];
      } catch (error) {
        // console.error("Error:", error);
        emp = [];
      }
    });
  
    async function deleteEmployee(id) {
      const response = await fetch(`http://localhost:3000/emp/${id}`, {
        method: "DELETE",
      });
  
      if (response.ok) {
        emp = emp.filter((employee) => employee.id !== id);
      }
    }
  
    async function updateEmployee(id, name,place) {
      await fetch(`http://localhost:3000/emp/${id}`, {
        method: 'PUT',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({ id, name, place }),
      });
      selectedEmployee = null;
    }
  
    export function selectEmployee(employee) {
      selectedEmployee = employee;
      empl.set(selectedEmployee)
    }

  </script>

  <div><input placeholder="filter prefix" bind:value={prefix}/></div><br>
  
  
  <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
    <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
      <tr>
        <th scope="col" class="px-6 py-3">ID</th>
        <th scope="col" class="px-6 py-3">Name</th>
        <th scope="col" class="px-6 py-3">Place</th>
        <th scope="col" colspan="3" class="act px-6 py-3">Actions allowed</th>
      </tr>
    </thead>
    <tbody>
      {#each filteredemp as employee}
        <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 hover:bg-gray-50 dark:hover:bg-gray-600">
          {#if selectedEmployee === employee}
          <td class="px-6 py-4">{employee.id}</td>
          <td class="px-6 py-4"><input type="text" bind:value={employee.name}/></td>
          <td class="px-6 py-4"><input type="text" bind:value={employee.place}/></td>
          <td class="px-6 py-4"><button on:click={() => updateEmployee(employee.id, employee.name,employee.place)}>
            Update
          </button></td>
          <td class="px-6 py-4"><button on:click={() => selectedEmployee = null}>
            Cancel
          </button></td>
          <td class="px-6 py-4"><button on:click={() => deleteEmployee(employee.id)}>Delete</button
            ></td>
            {:else}
            <td><a href="/show/topic" on:click={()=>selectEmployee(employee)}>{employee.id}</a></td>
            <td>{employee.name}</td>
            <td>{employee.place}</td>
            <td class="px-6 py-4"><button on:click={() => selectEmployee(employee)}>
              Edit
            </button></td>
          {/if}
        </tr>
      {/each}
    </tbody>
  </table>
  
  <style>
    tr,td{
        border: 5
    }
  </style>