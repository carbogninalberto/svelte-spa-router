<h1 id="catalog">Item {id}</h1>

<a id="previous" href use:link={`/catalog/${id - 1}`}>Previous</a>
<a id="next" href use:link={`/catalog/${id + 1}`}>Next</a>

<script>
    import { run } from 'svelte/legacy';

// Import the link action
// Normally, this would be: `import {link} from 'svelte-spa-router'`
import {link} from '../../../../Router.svelte'
    let { params } = $props();
let id = $state()
run(() => {
        if (params) {
        id = parseInt(params.id, 10)
    }
    });
</script>
