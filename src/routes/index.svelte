<script>
  import '@fontsource/montserrat';
  import '@fontsource/hind';
</script>

<svelte:head>
  <title>SvelteKit linting CSS Demo</title>
  <html lang="en-GB" />
  <meta
    name="description"
    content="SvelteKit CSS Stylelint: how you can lint vanilla CSS within your Svelte source files using stylelint accessibility and best practice rules."
  />
</svelte:head>

<main class="container">
  <div class="content">
    <h1>sveltekit-lint-css</h1>
    <p>SvelteKit linting CSS demo</p>
  </div>
</main>

<style>
  :global(html) {
    color: var(--colour-light);
  }

  :global(body) {
    margin: 0;
    font-family: Hind;
    font-weight: var(--font-weight-normal);
  }

  :global(:root) {
    --colour-theme: hsl(71 58% 64%); /* june bud */
    --colour-theme-lighter-20: hsl(71 58% 51%);
    --colour-light: hsl(60 24% 96%); /* baby powder */
    --colour-dark: hsl(25 29% 12%); /* black chocolate */
    --colour-dark-lighter-20: hsl(71 58% 10%); /* black chocolate */

    --font-weight-normal: 400;
    --font-weight-bold: 700;
  }

  .container {
    display: flex;
    min-height: 100vh;
    background-image: linear-gradient(
      to top right,
      var(--colour-theme-lighter-20),
      var(--colour-theme)
    );
  }

  .content {
    background-image: linear-gradient(
      to bottom left,
      var(--colour-dark-lighter-20),
      var(--colour-dark)
    );
    margin: 3rem 1.5rem auto;
    padding: 1.5rem 1rem;
    width: 100%;
    text-align: center;
  }

  .content h1 {
    font-family: Montserrat;
    font-size: 1.802rem;
    font-weight: var(--font-weight-bold);
  }

  .content p {
    font-size: 1.25rem;
  }

  @media (min-width: 768px) {
    .content {
      width: 640px;
      margin-left: auto;
      margin-right: auto;
      padding-top: 0;
    }
  }

  @media (min-width: 1024px) {
    .content {
      width: 768px;
    }
  }

  @media (min-width: 1280px) {
    .content {
      width: 1024px;
    }
  }
</style>
