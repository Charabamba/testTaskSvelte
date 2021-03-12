<script>
  function changeVisibility(e) {
    document
      .querySelector(".container")
      .querySelectorAll(".block")
      .forEach((item) => {
        item != e.target
          ? item.classList.add("block_visible")
          : item.classList.toggle("block_visible");
      });
  }
</script>

<div class="container">
  <div
    class="block block_visible"
    style="background: red"
    on:click={changeVisibility}
  />
  <div
    class="block block_visible"
    style="background: blue"
    on:click={changeVisibility}
  />
  <div
    class="block block_visible"
    style="background: green"
    on:click={changeVisibility}
  />
</div>

<style>
  .container {
    display: flex;
  }
  .block {
    width: 100px;
    height: 100px;
    opacity: 0;
  }
  .block_visible {
    opacity: 1;
  }
</style>
