<script lang="ts">
  import XkcdFetcher from './lib/xkcd_fetcher.svelte';
  import SocialBar from './lib/social_bar.svelte';
  import Bio from './lib/bio.svelte';
</script>

<main>
  <div class="bio">
    <Bio />
  </div>

  <div class="xkcd_fetcher">
    <XkcdFetcher />
  </div>
  
  <div class="social_bar">
    <SocialBar />
  </div>
</main>