<script>
    let { filterLabel } = $props();
</script>

<details>
  <summary>{filterLabel}</summary>
  <div class="dropdown-items">
    <ul>
      <li>First</li>
      <li>First</li>
      <li>First</li>
    </ul>
  </div>
</details>


<style>
    details {
    position: relative;
    display: inline-block;
  }
  
  .dropbtn {
    cursor: pointer;
  }

  .dropbtn:hover, .dropbtn:focus {
    color: #E84340;
  }
  
  .dropdown-items {
    position: absolute;
    background-color: #ffffff;
    min-width: 120px;
    border: solid 1px rgb(0, 0, 0);
    box-shadow: 0 0.5em 1em 0 rgba(0,0,0,0.2);
    border-radius: 3px;
    z-index: 1;
  }
  
  .dropdown-content button {
    font-weight: 900;
    width: 100%;
    color: rgb(22, 22, 22);
    padding: 12px 1em;
    text-align: center;
    background: none;
    border: none;
    cursor: pointer;
  }
  
  .dropdown-content button:hover {
    background-color: #dbdbdb;
  }

  .dropdown-content button:active {
    background-color: #dbdbdb;
    color: var(--accent-color);
  }
</style>