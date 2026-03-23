<script>
    let {
        imgSrc = '',
        altText = ''
        } = $props();
</script>

<img class="left-image" src="{imgSrc}" alt="{altText}" />

<style lang="scss">
  @use '$lib/styles' as *;

  :global(.story-theme) {
    .left-image {
      float: right;
      margin-left: var(--spacing-md);
      margin-bottom: var(--spacing-md);
      max-width: var(--max-width-xs);
      height: auto;
    }
  }
</style>