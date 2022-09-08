<script lang="ts" context="module">

</script>

<script lang="ts">
  import SEO from "svelte-seo";
  import Home from "$lib/pages/Home.svelte";
  import Footer from "$lib/pages/Footer.svelte";
 import Search from  "$lib/pages/Search.svelte";
/* basic colors at  https://tailwindcss.com/docs/customizing-colors   more at  https://hypercolor.dev/   */ 
  let primaryBackground = "bg-gradient-to-r from-slate-900 to-blue-900";
  let neutralBackground = "bg-neutral-200 dark:bg-neutral-900";
</script>

<SEO
  title="site name"
  description="site desc"
  canonical="link"
/>

<Home />
<!--About me/bio-->
<Search/>

<Footer  />
