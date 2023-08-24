<!-- src/routes/+layout.svelte -->
<script lang="ts">
	// import '../styles.css'
	import { invalidate } from '$app/navigation'
	import { onMount } from 'svelte'

	export let data

	let { supabase, session } = data
	$: ({ supabase, session } = data)

	onMount(async() => {
		// const { data, error } = await supabase.auth.signInWithOAuth({
  	// 	provider: 'discord'
		// })
		// console.log('data', data);
		// return () => data.subscription.unsubscribe()
	})
</script>

<svelte:head>
	<title>User Management</title>
</svelte:head>

<div class="container" style="padding: 50px 0 100px 0">
	<slot />
</div>