{#if staticProp}
  <p>We have a static prop: <b id="staticprop">{staticProp}</b></p>
{:else}
  <p>No static props here!</p>
{/if}

<script>

  /**
   * @typedef {Object} Props
   * @property {any} [staticProp] - Static props if they're set
   */

  /** @type {Props} */
  let { staticProp = null } = $props();
</script>