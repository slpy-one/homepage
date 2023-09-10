<script lang="ts">
  import { page } from "$app/stores";

  const Button = "p-4 hover:bg-ctp-overlay0 hover:text-ctp-base hover:opacity-60"

  const ActiveButton = `${Button}`
</script>

<div class="w-full fixed top-0 flex flex-row z-30">
  <div class="w-full justify-start text-left py-4">
    {#if $page.url.pathname == '/'}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class={ActiveButton}>
        slpy.one
      </a>
    {:else}
      <a href="/" class={Button}>
        slpy.one
      </a>
    {/if}
  </div>
  <div class="w-full justify-end text-right py-4">
    {#if $page.url.pathname == '/about'}
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a href="#" class={ActiveButton}>
        About
      </a>
    {:else}
      <a href="/about" class={Button}>
        About
      </a>
    {/if}
  </div>
</div>