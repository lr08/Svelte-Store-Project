<script>
  import "../app.css";
</script>

<div class="navbar">
  <nav class="container md:items-center">
    <ul>
        <li>
          <div class="flex items-center justify-between">
            <a
              class="text-xl font-bold hover:text-blue-400"
              href="/">About</a
            >
          </div></li>
          <li>
            <div class="flex items-center justify-between">
              <a
                class="text-xl font-bold hover:text-blue-400"
                href="/show">Details</a
              >
            </div></li>
      <li>
        <div class="flex items-center justify-between">
          <a class="text-xl font-bold hover:text-blue-400" href="/add"
            >Add Employee</a
          >
        </div>
      </li>
    </ul>
  </nav>
</div>

<div class="layout" data-name="root">
	<slot />
</div>

<style >
  .navbar {
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #fbf9f4;
    color: rgb(90 90 90);
  }

  .navbar ul {
    list-style: none;
    display: flex;
    gap: 10px;
  }

  .navbar ul li {
    padding: 5px;
  }
</style>
