<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";

  // Notes listing temporarily disabled while the page is under progress.
  /*
  import { page } from "$app/stores";
  import Post from "./Post.svelte";

  const notes = import.meta.glob("../../notes/*.md", {
    eager: true,
  }) as any;

  const images = import.meta.glob("../../notes/*.{png,jpg,svg}", {
    eager: true,
  }) as any;

  function trimName(id: string) {
    return id.match(/\.\.\/notes\/(.*)\.md$/)?.[1];
  }

  $: notesByDate = Object.keys(notes).sort((a, b) => {
    const dateA = notes[a].date ? new Date(notes[a].date).getTime() : 0;
    const dateB = notes[b].date ? new Date(notes[b].date).getTime() : 0;
    return dateB - dateA;
  });
  */
</script>

<Seo
  title="Shreeman's Notes"
  description="is a computer engineer, daydreamer, and a confused human."
/>

<section class="layout-md">
  <p class="text-sm md:text-lg mb-4">
    <em>
      Things I want to remember ∩ Things I don’t mind the internet knowing
    </em>
  </p>
  <hr class="my-8" />
  <p class="text-md md:text-lg mt-4">under work.</p>
</section>

<!--
<div class="notes flex flex-col">
  {#each notesByDate as id (id)}
    <section class="" id={trimName(id)}>
      <div class="mx-auto max-w-[1152px] px-4 sm:px-6">
        <Post data={notes[id]} {images} />
        <hr class="my-8" />
      </div>
    </section>
  {/each}
</div>
-->

<style lang="postcss">
</style>
