<script>
    import {empl} from "../empStore";

    let value;

empl.subscribe((storeValue) => {
  value = storeValue;
});
</script>

<!-- <p>{JSON.stringify(value)}</p> -->
<ul>
  <li>{value.id}</li>
<li>{value.name}</li>
<li>{value.place}</li>
</ul>
