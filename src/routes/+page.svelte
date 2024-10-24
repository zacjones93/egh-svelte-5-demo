<h1 class="text-2xl font-bold">Welcome to SvelteKit</h1>
<p>Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation</p>

{count}
{countTimesTwo}
<button class="bg-blue-500 text-white px-4 py-2 rounded-md"
onclick={() => (count += 1)}>Increment</button>
<button class="bg-red-500 text-white px-4 py-2 rounded-md"
onclick={() => (count -= 1)}>Decrement</button>


<script>
  let count = $state(0);

  let countTimesTwo = $derived(count * 2)

  $effect(() => {
    console.log(count)
  })

</script>
