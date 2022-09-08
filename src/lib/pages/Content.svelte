<script lang="ts">
  import Link from "$lib/components/Link.svelte";
  import Page from "$lib/components/Page.svelte";
  import Text from "$lib/components/Text.svelte";
  import { primaryBackground } from "$lib/utils/constants";

  export let backgroundClass = primaryBackground;
</script>

<Page id="content" title=" " {backgroundClass}>
  <Text>
    Content!
  </Text>
</Page>


<style>
  
</style>

