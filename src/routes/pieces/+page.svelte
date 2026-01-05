<script lang="ts">
  import { page } from "$app/stores";

  import Seo from "$lib/components/Seo.svelte";
  import Post from "./Post.svelte";

  const pieces = import.meta.glob("../../pieces/*.md", {
    eager: true,
  }) as any;

  const images = import.meta.glob("../../pieces/*.{png,jpg,svg}", {
    eager: true,
  }) as any;

  function trimName(id: string) {
    return id.match(/\.\.\/pieces\/(.*)\.md$/)?.[1];
  }

  $: piecesByDate = Object.keys(pieces).sort((a, b) => {
    const dateA = pieces[a].date ? new Date(pieces[a].date).getTime() : 0;
    const dateB = pieces[b].date ? new Date(pieces[b].date).getTime() : 0;
    return dateB - dateA;
  });
</script>

<Seo
  title="Shreeman's Pieces"
  description="is a computer engineer, daydreamer, and a confused human."
/>

<section class="layout-md">
  <div class="text-sm md:text-lg mb-4">
    <em> "Who in the world am I? Ah, that's the great puzzle." </em>
    <span class="text-sm text-neutral-500">
      ― Lewis Carroll, Alice in Wonderland</span
    >
  </div>
  <hr />
  <p class="mt-4 mb-4">under work.</p>
  <p class="mb-4" />
  <p class="mb-4" />
  <p class="mb-4" />
  <hr class="my-8" />
</section>

<div class="pieces flex flex-col">
  {#each piecesByDate as id (id)}
    <section class="" id={trimName(id)}>
      <div class="mx-auto max-w-[1152px] px-4 sm:px-6">
        <Post data={pieces[id]} {images} />
        <hr class="my-8" />
      </div>
    </section>
  {/each}
</div>

<style lang="postcss">
</style>
