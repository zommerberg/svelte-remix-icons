# Description

This is a sveltekit icon library based on remixIcons. Highly inspired by svelte-hero-icons

- complete remixions set optimized for svelte
- programatically change filled or line version based on the filled attribute
- fully typed for a great IDE experience
- works with SvelteKit & Vite

## Configuration

```
const config = {
  // other vite-plugin-svelte config
  kit: {
    // other svelte-kit config
    vite: {
      // other vite config
      optimizeDeps: {
        include: ["svelte-remix-icons"],
      },
    },
  },
};
export default config;
```

## Usage

```
<script>
  // Only import what you need!
  import { ArrowRight } from 'svelte-remix-icons'

  // For now you have to import the icon component like this:
  import RemixIcon from 'svelte-remix-icons/RemixIcon.svelte'
</script>

<!-- use filled attribute to control whether to show filled or outline version of icon -->
<Icon src="{ArrowRight}" filled />

<!-- use size attribute to set icon size (32 -> 32px | 2rem | 100% == default ) -->
<Icon src="{ArrowRight}" size="32" />

<!-- use Windi CSS or tailwindcss classes directly -->
<Icon src="{ArrowRight}" class="w-6 h-6 text-red-500" />
```
