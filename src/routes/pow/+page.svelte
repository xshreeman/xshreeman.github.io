<script lang="ts">
  import Seo from "$lib/components/Seo.svelte";
  import Workplace from "./Workplace.svelte";
</script>

<Seo
  title="Shreeman's Proof of Work"
  description="is a computer engineer, daydreamer, and a confused human."
/>

<section class="layout-md py-6">
  <h2 class="heading2">Proof of Work</h2>

  <Workplace
    title="Volunteer"
    company="Corroboration and Review Committee"
    dates="October 2025 – Present"
    location="Pilani, India"
  >
    <li>Corroborating finances of Student's Union, Annual Cultural Fest and Annual Tech Fest in College.</li>
    <li>Funds under management exceeding 5cr INR (or 600k USD)</li>
    
  </Workplace>
</section>

<section class="layout-md py-6">
  <h2 class="heading2">Education</h2>

  <div class="mb-4">
    <div class="flex justify-between items-end">
      <h3 class="text-black text-lg">Birla Institute of Technology and Science Pilani, Pilani Campus</h3>
      <div class="text-neutral-500 mb-0.5">Aug 2024 — May 2029*</div>
    </div>
    <p class="byline">
      Integrated Dual Degree - Bachelor of Engineering, Electronics and Communication Engineering and Masters in Physics
    </p>
  </div>
</section>

<style lang="postcss">
  .byline {
    @apply font-serif italic;
  }
</style>
