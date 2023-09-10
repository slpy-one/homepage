<script lang="ts">
  import TW from "../lib/constant/tailwind";
  import slpyService from "../lib/db/services";
</script>

<svelte:head>
  <title>slpy.one</title>
</svelte:head>

<section class="md:w-[80%] w-full min-h-screen flex flex-row items-center justify-center text-center mx-auto">
  <div class="h-[70vh] w-full overflow-y-auto">
    <h1 class={`${TW.heading.xxxl}`}>
      slpy one | Services
    </h1>
    <div class="w-[80%] flex flex-row flex-wrap justify-center text-center gap-4 mx-auto">
      {#each slpyService as service}
        <a class="block w-[100%] md:w-[40%] h-auto py-4 border-2 text-lg rounded hover:opacity-60" href={service.url} target="_blank">
          {service.name}
        </a>
      {/each}
    </div>
  </div>
</section>