<script lang="ts">
  import TW from "$lib/constant/tailwind";
  import teams from "$lib/db/team";
</script>

<section class="md:w-[80%] w-full min-h-screen flex flex-row items-center justify-center text-center mx-auto">
  <div class="h-[70vh] w-full overflow-y-auto">
    <h1 class={`${TW.heading.xxxl} underline !py-4`}>
      About
    </h1>
    <p class="w-full md:w-[50%] mx-auto text-[18px]">
      This project is an project that unite every discord services that we found on elsewhere separately into 1 big service and split it into various small service that can help every user who try to use this website can find their service easily :)
    </p>

    <div class="py-2"></div>

    <h1 class={`${TW.heading.xxxl} underline !py-4`}>
      Our Team
    </h1>
    <div class="w-full md:w-[80%] mx-auto flex flex-row flex-wrap justify-center text-center gap-4">
      {#each teams as team}
        <a class="member-card w-[18rem] h-[18rem] bg-ctp-overlay0 flex flex-col items-center rounded hover:scale-95" href={`https://github.com/${team.username}`} target="_blank">
          <div class="pics w-[18rem] h-full !bg-cover !bg-no-repeat !bg-center rounded-t" style={`background: url(${team.pics})`}></div>
          <div class="text h-[0px] w-full p-4 text-left rounded-b opacity-0 backdrop-opacity-40">
            <p class={`${TW.heading.xxl} !py-1 w-auto`}>
              {team.name}
            </p>
            <p class={`${TW.heading.l} text-ctp-subtext0 !py-1 w-auto`}>
              {team.username}
            </p>
          </div>
        </a>
      {/each}
    </div>
  </div>
</section>

<style>
  .member-card:hover > .pics, .member-card:hover > .text {
    height: 50%;
  }

  .member-card:hover > .text {
    opacity: 1;
  }
</style>