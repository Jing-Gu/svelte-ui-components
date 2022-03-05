<script>
  export let color
  export let size
  export let format

</script>

<button class='btn {color} {size} {format}'>
  <slot></slot>
</button>

<style>
	.btn {
    display: flex;
    align-items: center;
    font-size: 1rem;
		padding: .5rem 1rem;
    cursor: pointer;
    border: none;
    border-radius: 6px;
    transition: all 300ms ease-in-out;
	}

  .btn.small {
    font-size: .875rem;
    padding: .5rem .75rem;
  }

  .btn.icon-round {
    border-radius: 50px;
    padding: 1rem;
    display: grid;
    place-items: center;
    color: #fff;
  }

  .btn.icon-round.small {
    padding: .75rem;
  }

  .primary-blue {
    background: var(--blue-500);
    color: var(--blue-900);
  }

  .primary-blue:hover {
    background: var(--blue-700);
    color: var(--blue-500)
  }

  .primary-blue:focus {
    border: 4px solid var(--blue-300);
    background: var(--blue-700);
    color: var(--blue-500)
  }

  .primary-yellow {
    background: var(--yellow-500);
    color: var(--yellow-900);
  }

  .primary-yellow:hover {
    background: var(--yellow-700);
    color: var(--yellow-500);
  }
  .primary-yellow:focus {
    border: 4px solid var(--yellow-300);
    background: var(--yellow-700);
    color: var(--yellow-500);
  }

  .secondary-blue {
    border: 2px solid var(--blue-500);
    background: transparent;
    color: var(--blue-500);
  }
  .secondary-blue:hover {
    border: 2px solid var(--blue-500);
    background: var(--blue-500);
    color: #fff;
  }
  .secondary-blue:focus {
    border: 4px solid var(--blue-500);
  }
  .secondary-yellow {
    border: 2px solid var(--yellow-500);
    background: transparent;
    color: var(--yellow-500);
  }
  .secondary-yellow:hover {
    border: 2px solid var(--yellow-500);
    background: var(--yellow-500);
    color: #fff;
  }
  .secondary-yellow:focus {
    border: 4px solid var(--yellow-500);
  }

  .tertiary {
    color: var(--coolgrey-500);
    background: transparent;
  }
  .tertiary:hover {
    background: var(--coolgrey-100);
  }
  .tertiary:focus {
    border: 4px solid var(--coolgrey-500);
    background: var(--coolgrey-100);
  }

  .disabled {
    background: var(--neutral-100);
    color: var(--neutral-300);
    cursor: not-allowed;
  }
</style>


<svelte:options tag='car-button' />