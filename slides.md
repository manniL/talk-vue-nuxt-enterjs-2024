---
theme: ./theme
title: "Nuxt 3 - The Present and the Future"
website: lichter.io
handle: TheAlexLichter
favicon: https://lichter.io/img/me@2x.jpg
highlighter: shiki
lineNumbers: true
layout: intro
transition: fade
---

# Web Development changes quickly...

---
layout: intro
---

# ...and that causes discussions and drama/fights

<!-- 
Like the night session yesterday but different!
-->

---

<img src="/let-vs-const.jpg" class="mx-auto scale-120 h-100" />

<!--

let vs. const

* always const as no re-assignment
-->

---

# Tailwind vs. "Semantic CSS"

<img src="/tailwind-vs-semantic-bullshit.png" class="mx-auto h-80" />

<p v-click class="absolute top-60 left-70 text-red-600 font-bold text-[80pt] rotate-25">Bullshit!</p>

---

---

<img src="/no-build.jpg" class="mx-auto scale-120 h-100" />

<!--
DHH saying No build
-->

---

<img src="/bullshit.jpg" class="mx-auto scale-120 h-100" />


---
clicks: 2
---

<div class="flex flex-wrap justify-center items-center w-full h-90" :class="{'pt-16': $clicks !== 0}">
  <TransitionGroup name="list">
    <div key="logos-angular-icon" class="flex flex-col items-center">
      <logos-angular-icon  class="text-8xl my-4 mx-7" />
      <p class="text-2xl" v-if="$clicks >= 1">Angular</p>
    </div>
    <logos-remix-icon key="logos-remix-icon" class="text-8xl my-4 mx-7 stroke-width-2 stroke-white" v-if="$clicks === 0" />
    <logos-solidjs-icon key="logos-solidjs-icon" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <logos-qwik-icon key="logos-qwik-icon" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <logos-nextjs-icon key="logos-nextjs-icon" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <div key="logos-vue" class="flex flex-col items-center" :class="{'-mt-32': $clicks === 2}">
      <logos-vue class="text-8xl my-4 mx-7" />
      <p class="text-2xl" v-if="$clicks >= 1">Vue.js</p>
    </div>
    <logos-preact key="logos-preact" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <logos-inferno key="logos-inferno" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <logos-astro-icon key="logos-astro-icon" class="text-8xl my-4 mx-7 stroke-width-2 stroke-white" v-if="$clicks === 0" />
    <logos-lit-icon key="logos-lit-icon" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <logos-nuxt-icon key="logos-nuxt" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <logos-stenciljs-icon key="logos-stenciljs-icon" class="text-8xl my-4 mx-7 stroke-width-2 stroke-white" v-if="$clicks === 0" />
    <logos-svelte-icon key="logos-svelte-icon" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
    <div key="logos-react" class="flex flex-col items-center">
      <logos-react class="text-8xl my-4 mx-7"  />
      <p class="text-2xl" v-if="$clicks >= 1">React</p>
    </div>
    <logos-analog key="logos-analog" class="text-8xl my-4 mx-7" v-if="$clicks === 0" />
  </TransitionGroup>
</div>

<style>
.list-move, /* apply transition to moving elements */
.list-enter-active,
.list-leave-active {
  transition: all 0.5s ease;
}

.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(30px);
}

/* ensure leaving items are taken out of layout flow so that moving
   animations can be calculated correctly. */
.list-leave-active {
  position: absolute;
}
</style>

---
layout: intro
---

# Drama in Angular?

<logos-angular-icon class="mx-auto text-8xl mt-8" />

<!--
Angular Renaissance
Perf
-->

---

<img src="/rxjs-signals.jpg" class="mx-auto scale-120 h-100" />

---

<img src="/angular-wiz.jpg" class="mx-auto scale-120 h-100" />

---
layout: intro
---

# Drama in React?

<logos-react class="mx-auto text-8xl mt-8" />

---

<img src="/react-fetch.jpg" class="mx-auto scale-120 h-100" />

---

<img src="/react-fetch-back.jpg" class="mx-auto scale-120 h-100" />

---

<img src="/react-patch-date.jpg" class="mx-auto scale-120 h-80" />

---

<img src="/next-vs-remix.jpg" class="mx-auto" />

<!--

* Vercel gives up on Edge
  * How it started https://twitter.com/rauchg/status/1546913927325310976
  * How it is going https://twitter.com/leeerob/status/1780705942734331983
* Vercel is "taking over" React

-->

---
layout: intro
clicks: 1
---

# Drama in Vue.js?


<Crickets v-if="$clicks === 0" class="mx-auto text-8xl mt-8">
<logos-vue />
</Crickets>
<logos-vue v-else class="mx-auto text-8xl mt-8" />

---
layout: intro
---


# A <logos-vue/>ue <span class="text-[#41b883]">Ahead</span>

## Plans and Developments of the Progressive Framework

<br><br>

### enterJS 2024

---
layout: two-cols
heading: About me
---

<template v-slot:default>
<div class="flex flex-col justify-center items-center h-full">
  <img class="w-75 rounded-full" src="https://lichter.io/img/me@2x.webp" />
  <h2 class="mt-4">Alexander Lichter</h2>
</div>
</template>

<template v-slot:right>
<VClicks class="space-y-2 mt-10 text-xl h-full">

* <mdi-account-check class="dark:text-green-100 text-green-700" /> **Web Engineering Consultant**
* <mdi-microphone /> Speaker &bull; Instructor &bull; Podcast Host
* <logos-nuxt-icon /> Nuxt.js Team
* <mdi-twitter class="text-blue-400" /><mdi-youtube class="text-red-500" /><mdi-twitch class="text-purple-700" /> @TheAlexLichter
* <mdi-web /> [https://lichter.io](https://lichter.io)
* <mdi-github /> [manniL](https://github.com/manniL)

</VClicks>
</template>

---
layout: intro
---

# Drama in Vue.js?

<logos-vue class="mx-auto text-8xl mt-8" />

---
preload: false
---

<img v-motion :initial="{ y: 500 }" :enter="{ y:0, transition: { duration: 1000 } }" src="/angry.png" />


---

<img src="/options-api.jpg" class="mx-auto scale-120 h-90" />

---

<img src="/nuxt-rewriting.jpg" class="mx-auto scale-120 h-90" />

---

<img src="/nuxt-waiting.jpg" class="mx-auto scale-120 h-90" />

---
layout: intro
---

# Besides that, no "drama" in the Vue.js community!

<VClick>

## Let's check spicy topics

</VClick>

---
layout: intro
---

# Will the Options API go away?

---

# Will the Options API go away?

<VClicks>

* No, it won't! It is still supported and there are no deprecation plans
* **BUT**: The Composition API is the future
* Focus of the "ecosystem"
* We will also see another reason later

</VClicks>

---
layout: intro
---

# Signals in Vue? 

---

# Signals in Vue? 

<VClicks depth="2">

* `const [count, setCount] = createSignal(0);` - No?!
* Vue has "Signals baked in" as `ref` and `shallowRef`
* Deep tracking reactivity already built in since the Composition API
* Signals can be [created in less than 12 lines of code with it](https://play.vuejs.org/#eNp9Uk1v1DAQ/SsjXzYRS0IFp1WyBaoe4ACo5Vb3ELKTrFvHDv4Ii1b574ydTZZWVS+RPe+N572XObJPfZ8NHtmGFbY2ondg0fl+y5Xoem0cHKE2WDm8Fa2qJIzQGN3BKsutlmL31sZy9mBXXHFVa2Ud3NXaK7cOL12F0z2UTx5J3qVcFfk0jybRxWHXSyLQDaDYX2yPNDf0JimMY5FTJSK/vHNawcdaivqx5GwekQxQbmGAN3CRcha5AELR1A6Vi6351EtYkS/j2Jo980FJLM7tvpJS/7nBZg3OiLZFQ+clA8otusZD5Dde1U6Quideh0p6XIPuA2RTOAYxU06GcjmPmJiUzAy36IhAAZAzk0X0DJLxAA4RjW/CTKK6+9ujbiiPsixhNQtbwSUMyYmVwgaGU04NJCd9lxn+9pW0sbGhA/HOzhMT5Y3hY2hNjII7Uhn/9D1XI6XpLOlrREtJakVZRmmc1brrhUTzfRrD2WYWzVkM4GusOUNZzfV6j/XjC/UHewg1zn4YtGgG5GzBXGVI0ARf337DA50XsNM7L4n9CniDtA4+aJxon73akez/eFHtl7ghQrU/7fXBobKzqSA0RhT5nNGKXL1i/Sz3ffbhFO3Ixn8p0jK5)

</VClicks>

<Code file="solid-signals.ts" v-click>

```ts
import { shallowRef, triggerRef } from 'vue'

export function createSignal(value, options) {
  const r = shallowRef(value)
  const get = () => r.value
  const set = (v) => {
    r.value = typeof v === 'function' ? v(r.value) : v
    if (options?.equals === false) triggerRef(r)
  }
  return [get, set]
}
```

</Code>

---

# Signals in Vue?

````md magic-move
```vue
<script setup>
import { createSignal } from './solid-signal.js'

const [count, setCount] = createSignal(0)
</script>

<template>
  <h1>{{ count() }}</h1>
  <button @click="setCount(v => v + 1)">
    increment
  </button>
</template>
```
```vue
<script setup>
import { ref } from 'vue'
const count = ref(0) // or shallowRef without deep reactivity
</script>

<template>
  <h1>{{ count }}</h1>
  <button @click="count++">
    increment
  </button>
</template>
```
````

<VClicks depth="2">

* No fn calls, less verbose
* But: can't pass "only the signal getter" (except using `readonly(count)`)
* Ref unwrapping in the template (no `.value`)
* **Matter of preference**

</VClicks>

---
layout: intro
---

# Vue Server Components?

---

# Vue Server Components?

<VClicks>

* React went "server-first" - but what about Vue?
* **No**! Won't happen in the same way!
* Exploration should be done in the Meta Framework => Nuxt <logos-nuxt-icon/>

</VClicks>

---
layout: intro
---

# How old is Vue now?

---
layout: intro
---

# 10 Years <span class="text-[#41b883]">Vue</span>!

<img v-click src="/vuejs-uwu.png" class="mx-auto -mt-8 h-80" />

---
layout: intro
---

# Vue = Boring Tech

---

# Vue = Boring Tech

<VClicks depth="2">

* No drama
* It just works
* It's stable and reliable
* "One way" to do things, e.g. for:
  * Routing
  * State Management
* One main API to use (Composition API with `<script setup>` if compiler is used)
  * While still supporting Options API
* Steady improvements

</VClicks>

---
layout: intro
---

# Which features shipped since the Vue 3 release (2020)?

---

# Which features shipped since the Vue 3 release?

<VClicks depth="2">

* Migration Build (v3.1)
* `<script setup>` was stabilized (v3.2)
* `v-bind` in `<style>` was stabilized (v3.2)
* `v-memo` was introduced (v3.2)
* Introduction of Reactivity Transform (v3.2)
* Generic components (v3.3)
* Reactivity Transform was dropped (v3.3)
  * But reactive destructured props were kept (experimental)
* Experimental `defineModel` macro (v3.3)
* Stable `defineModel` (v3.4)
* `:abc="abc"` shorthand `:abc` (v3.4)

</VClicks>

---

# What else happened?

<VClicks depth="2">

* Of course, bugs were fixed and things were improved
* **Performance gains**
  * 2x faster template parser
  * SSR improvements (after the viral benchmarks)
  * Various reactivity improvements (less mem, less rerenders etc.)
  * More to come!

</VClicks>

---
layout: intro
---

# What about the future of Vue?

---

# What about the future of Vue?

<VClicks depth="2">

* Lazy hydration support
  * Planned for Vue 3.5
  * Also further SSR improvements in the works
* Vue Router [Data Loaders](https://uvr.esm.is/rfcs/data-loaders/)
  * Better data fetching
  * Should reduce complexity
  * And enforce best practices
* Pinia Colada

</VClicks>

---

# Data Loaders


````md magic-move
```vue
<script setup lang="ts">
import { getUserById } from '../api'

// Exporting is important!
export const useUserData = defineLoader(async (route) => {
  const user = await getUserById(route.params.id as string)
  // do whatever you want here
  return user
})
</script>
```
```vue
<script setup lang="ts">
import { getUserById } from '../api'

// Exporting is important!
export const useUserData = defineLoader(async (route) => {
  const user = await getUserById(route.params.id as string)
  // do whatever you want here
  return user
})

// Access the fetched data and state
const { data: user, isLoading, error, reload } = useUserData()
</script>
```
````

---

# Pinia Colada

<div class="flex justify-around items-center">
  <logos-pinia class="text-[160pt]"  />
  <img v-click src="/pinia-colada.png" class="h-90">
</div>

---

# Pinia Colada

<VClicks>

* Smart data fetching layer for Pinia
* Think of it as Vue Query for pinia stores
* Still experimental but worth trying out!

</VClicks>

---
layout: intro
---

# 🥁🥁🥁 Vapor Mode 🥁🥁🥁

---

# 🥁🥁🥁 Vapor Mode 🥁🥁🥁

<VClicks>

* Alternative to VDOM in Vue
* <logos-solidjs /> Solid-like approach to render components
* Blazing fast™️
* Still experimental and in development
* Already open source + [API progress available](https://github.com/vuejs/core-vapor/issues/197)

</VClicks>

---
layout: intro
---

# [Let's have a look!](https://play.vuejs.org/#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)

---
layout: intro
---

# <logos-vue /> is the only mainstream framework which is independent*

\*As in: not dominantly owned / backed by a single corp!

---

<img src="/vue-for-us.jpg" class="mx-auto scale-120 h-90" />

---

# What did <logos-vue/>ue ever done for us?

<VClicks depth="2">

* Vite <logos-vitejs />
  * [Rolldown](https://rolldown.rs/) <img src="https://rolldown.rs/rolldown-round.svg" class="h-10 w-10 inline" />
* Volar (Language Tools) <img src="https://raw.githubusercontent.com/volarjs/docs/main/public/favicon.svg" class="h-10 w-10 inline" />
* [UnJS](https://unjs.io/relations/) <img src="https://unjs.io/assets/images/design-kit/unjs-logo-black.svg" class="h-8 w-8 inline" />
* [Slidev](https://sli.dev/) <img src="https://sli.dev/logo.png" class="h-8 w-8 inline" /> (this presentation is built with it!)

</VClicks>

<style>
  ul {
    @apply !mt-8;
  }
  li {
    @apply !text-3xl my-6;
  }
</style>

<!--

Vite is used by all major framework except "one weirdo" :P
Rolldown: Rust-based Rollup
More to come with OXC
Full toolchain in the future (linter/format/...)

-->

---
layout: intro
---

# <logos-nuxt-icon/> Nuxt <span class="text-[#00DC82]">3</span>

---

# <logos-nuxt-icon/> Nuxt <span class="text-[#00DC82]">3</span>

<VClicks>

* Meta Framework based on Vue.js
* Versatile (SPA/SSR/SSG/ISR/Hybrid)
* Own Server Engine (Nitro)
  * Used by frameworks around the world (Analog, SolidStart, ...)
* Convention over Configuration, sane defaults
* More comfort, reduced "Time To Market"

</VClicks>

---

# <logos-nuxt-icon/> Nuxt <span class="text-[#00DC82]">3</span> Features


<VClicks>

* FS-based routing
* Anti-pattern detection
* Deploy "anywhere"
* Full Stack possibilities with server routes and API routes
* Layers - "inherit" from other (partial) apps
* Server Components (experimental)
* Rendering in various modes in the same app (hybrid)
* Outstanding DevTools
* Nuxt Hub (<logos-cloudflare-icon /> integration with D1, KV, Blob)

</VClicks>

---
layout: intro
---

<img src="/nuxt-uwu.png" class="mx-auto scale-120 h-90" />

# Demo!

---
layout: intro
---

# <logos-nuxt-icon/> Nuxt <span class="text-[#00DC82]">4</span>

---

# <logos-nuxt-icon/> Nuxt <span class="text-[#00DC82]">4</span>

<VClicks depth="2">

* Was planned for Q1, moved to Q2 because other things had to ship first
* New goal: "Nuxt v4 on or before June 14"
  * Depends on various UnJS major versions (e.g. Nitro)
* 6 months support + bug fixes for Nuxt v3 from that point on

</VClicks>

---
layout: intro
---

# <span class="text-[#00DC82]">Features</span> in Nuxt <span class="text-[#00DC82]">4</span>

<VClicks>

## Which big features are coming?

</VClicks>

---
layout: intro
---

# NONE

---

# NONE


* Amazing features in every minor release

<VClicks>

* Major release = Breaking changes

</VClicks>

---
layout: intro
---

# Breaking Changes

<img class="mx-auto" src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExd3hvdG1jaWFoYW81anMyOGJpZjZmOGl4OTk3eHA4N2Zuc3loNzgycSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l2Je2ifGlRZEWDbb2/giphy.gif" v-click>

---
layout: intro
---

# Who is still traumatized by

<VClicks>

## Vue 2 -> Vue 3

</VClicks>

<VClicks>

## Nuxt 2 -> Nuxt 3

</VClicks>

<style>
h2 {
  @apply !text-4xl !mt-8;
}
</style>

---
layout: intro
---

<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExeW8zbDlseGF2czd1c2YwZmh4Nzc3bTR2a3J0cXlhcjd0OGh3Nm50NSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/PMUooKtzGNjsPXkQUJ/giphy.gif" class="mx-auto">

---

# Breaking Changes


<VClicks depth="2">

* So, what should we expect?
* A migration like Nuxt 2 to Nuxt 3?

</VClicks>

---
preload: false
---

<img v-motion :initial="{ y: 500 }" :enter="{ y:0, transition: { duration: 1000 } }" src="/angry.png" />

---

# No! Don't worry!

<VClicks depth="2">

* A [list](https://github.com/nuxt/nuxt/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A4.x) of smaller breaking changes
  * Non-exhaustive
* More to come
* But in no way comparable to version three

</VClicks>

---
layout: intro
---

# How can the team help?

---

# How can the team help?

<VClicks>

* We will provide an extensive migration guide
* We plan on providing code mods / a migration wizard
* `future` flag to enable breaking changes before they'll happen

</VClicks>

---
layout: intro
---

# Why Nuxt 3 was "different"

---

# Why Nuxt 3 was "different"

<VClicks>

* TS rewrite
* New internal architecture
* Fresh server engine
* Switching from Webpack 4 to Vite (while still supporting 5)
* Switching from Vue 2 to Vue 3
* Dealing with the Composition API
* Pushing the ecosystem forward

</VClicks>

---
layout: intro
---

# Nuxt 4 = None of these kind of changes

---

# Nuxt 4 = None of these kind of changes

<VClicks depth="2">

* The chance for the team to introduce breaking changes
  * e.g. to remove legacy code
  * or to enable sensible defaults
  * And so on

</VClicks>

---
layout: intro
---

# Let's <span class="underline"> **not** </span> make majors a **marketing thing**

---
layout: intro
preload: false
---

<img v-motion class="mt-14" :initial="{ y: 500 }" :enter="{ y:0, transition: { duration: 1000 } }" src="/happy.png" />


---
layout: intro
---

# <span class="text-[#00DC82]">More</span> Features

---

# <span class="text-[#00DC82]">More</span> Features

<VClicks depth="3">

* More work on experimental features:
  * Server Components
  * Typed Pages
  * Nitro experimentals
    * Tasks
    * DB0
    * crossws
  * and so on

</VClicks>

---
layout: intro
---

# <span class="text-[#00DC82]">Upcoming</span> Features (core)

---

# <span class="text-[#00DC82]">Upcoming</span> Features (core)

<VClicks depth="2">

* `onPreHydrate`
* Built-in build cache
* Make Multi App Support possible
* Various other thing I can't name here ;)

</VClicks>

---
layout: intro
---

# <span class="text-[#00DC82]">Upcoming</span> Features (non-core)

---

# <span class="text-[#00DC82]">Upcoming</span> Features (non-core)

<VClicks depth="2">

* Nuxt Module for Third Party Handling
* Nuxt Fonts Module 
  * Wait, this is already out!
* Perf Hints Module
* a11y Module
* Render Markdown in Nuxt straight away
  * Wait, this is also already out!

</VClicks>

---

# Psyched? Then keep up to date!

<div class="flex mx-32 my-auto justify-around">

<Qrcode class="max-w-xl" url="https://www.youtube.com/@TheAlexLichter/" note="My YouTube Channel" />
<Qrcode class="max-w-xl" url="https://dejavue.fm/?ref=enterjs" note="The DejaVue Podcast" />

</div>

---
layout: intro
---

# Thanks a lot to my sponsors!
<img src="https://raw.githubusercontent.com/manniL/static/main/sponsors.svg" class="h-80 mx-auto" alt="My GitHub sponsors">

---
layout: two-cols
heading: Thank you for your attention!
---

<template v-slot:default>
<div class="flex flex-col justify-center items-center h-full">
<img
  class="w-75 rounded-full"
  src="https://lichter.io/img/me@2x.webp"
  />
  <h2 class="mt-4">Alexander Lichter</h2>
</div>
</template>

<template v-slot:right>

* <mdi-account-check class="dark:text-green-100 text-green-700" /> **Web Engineering Consultant**
* <mdi-microphone /> Speaker &bull; Instructor &bull; Podcast Host
* <logos-nuxt-icon /> Nuxt.js Team
* <mdi-twitter class="text-blue-400" /><mdi-youtube class="text-red-500" /><mdi-twitch class="text-purple-700" /> @TheAlexLichter
* <mdi-web /> [https://lichter.io](https://lichter.io)
* <mdi-github /> [manniL](https://github.com/manniL)

</template>

<style>
  ul {
    @apply space-y-2 mt-10 text-xl h-full;
  }
</style>