<script lang="ts">
  import Intro from "./Components/Intro.svelte";
  import Links from "./Components/Links.svelte";
  import ToggleMode from "./Components/ToggleMode.svelte";
  import SvelteSeo from "svelte-seo";
  export let name: string, username: string, avatarUrl: any, url: any;
  console.log(url);
</script>

<SvelteSeo
  description="Linktree of @{username}"
  openGraph={{
    title: `@${username} | Linktree`,
    description: `Linktree of @${username}`,
    type: `website`,
  }}
  twitter={{
    title: `@${username} | Linktree`,
    description: `Linktree of @${username}`,
    site: `@gifaldyazkaa`,
  }}
/>

<Intro propsName={name} propsUsrname={username} propsAvatarUrl={avatarUrl} />
<Links propsUrl={url} />
<ToggleMode />

<style>
</style>
