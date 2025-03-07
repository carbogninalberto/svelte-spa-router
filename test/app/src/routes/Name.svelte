<h2 class="routetitle">Hi there!</h2>

<p id="nameparams" onclick={() => dispatch('routeEvent', {action: 'hi', params})}>Your name is: <b>{params.first}</b> <b>{#if params.last}{params.last}{/if}</b></p>
<p><em>Hint:</em> Try changing the URL and add your name, e.g. <code>/hello/jane/doe</code></p>

<script>

// Event dispatcher for the custom "routeEvent" event
import {createEventDispatcher} from 'svelte'
	let { params = {} } = $props();
const dispatch = createEventDispatcher()
</script>
