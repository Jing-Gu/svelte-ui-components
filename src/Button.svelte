<script>
  export let count = 0
  export let color = 'secondary'

  const handleClick = () => {
    count = +count + 1
  }
</script>

<button on:click={handleClick} class={color}>Count {count}</button>

<style>
	button {
		padding: 1rem 2rem;
	}
  .primary {
    background: blue;
    color: #fff;
  }
  .secondary {
    background: #ff6a95;
  }
</style>


<svelte:options tag='car-btn' />