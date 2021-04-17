# Best Practices Et Cetera
A running list of best practices, guides and tutorials.

[Important Concepts](https://github.com/jendiamond/best-practices/blob/master/README.md#important-concepts) | 
[Get better at](https://github.com/jendiamond/best-practices/blob/master/README.md#be-better-at) | 
[Useful tools](https://github.com/jendiamond/best-practices/blob/master/README.md#useful-tools-review-each) | 
[Good reading](https://github.com/jendiamond/best-practices/blob/master/README.md#good-reading) | 
[Cheatcheets](https://github.com/jendiamond/best-practices/blob/master/README.md#cheatcheets) | 
[Tutorials](https://github.com/jendiamond/best-practices/blob/master/README.md#tutorials)

## Overview

1. [Roadmap](https://github.com/UCLALibrary/library-website-nuxt/wiki/Roadmap)
1. [Website Development Process](https://github.com/UCLALibrary/library-website-nuxt/wiki/Website-Development-Process)

## Guides

1. [How to write a Component Request](https://github.com/UCLALibrary/library-website-nuxt/wiki/How-to-write-a-Component-Request)
1. [How to build a component for UCLA Library](https://github.com/UCLALibrary/library-website-nuxt/wiki/How-to-build-a-component-for-UCLA-Library)
1. [How to submit a component for review](https://github.com/UCLALibrary/library-website-nuxt/wiki/How-to-submit-a-component-for-review)

## Docs
+ [Vue 2](https://vuejs.org/v2/)

## Tools (Review each)
- [ ] [Demystifing Nth-Child in CSS](http://www.nealgrosskopf.com/tech/resources/80/)
- [ ] [Flexy Boxes Playground](https://the-echoplex.net/flexyboxes/)
- [ ] [CSS Grid Generator](https://cssgrid-generator.netlify.com/)
- [ ] [16:9 calculator](https://www.size43.com/16by9-aspect-ratio-calculator/)
- [ ] [Clippy](https://bennettfeely.com/clippy/)
- [ ] [Facebook OG debugger](https://developers.facebook.com/tools/debug/)
- [ ] [Code Drops](https://codedrops.io/)

## Read
- [ ] [Vue Style Guide](https://vuejs.org/v2/style-guide/)
- [ ] [The introduction to Reactive Programming you've been missing](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)
- [ ] [You (Might) Don't Need jQuery](https://github.com/nefe/You-Dont-Need-jQuery)
- [ ] [A Smashing Guide To The World Of Search Engine Optimization](https://www.smashingmagazine.com/smashing-guide-search-engine-optimization/)
- [ ] [Good overview of ES6 destructuring](https://2ality.com/2015/01/es6-destructuring.html)
- [ ] [A good book on how to write good CSS](https://maintainablecss.com/)
- [ ]  [Use console.log() like a pro](https://markodenic.com/use-console-log-like-a-pro/)

## Cheatcheets (Review)
- [ ] https://www.vuemastery.com/pdf/Nuxtjs-Cheat-Sheet.pdf
- [ ] https://www.vuemastery.com/pdf/Vue-Essentials-Cheat-Sheet.pdf

## Tutorials
### CSS

#### Flex
- [ ] https://the-echoplex.net/flexyboxes/
- [ ] http://flexboxfroggy.com/

### CSS Grid
- [ ] [CSS Grid Generator](https://cssgrid-generator.netlify.app/)

## Vue
### [Intro to Vue 2](https://www.vuemastery.com/courses/intro-to-vue-js/vue-instance/)
### Components
- [ ] https://frontstuff.io/build-your-first-vue-js-component

## Nuxt
- [ ] https://nuxtjs.org/docs/2.x/features/nuxt-components
- [ ] https://openbase.com/js/nuxt/tutorials
- [ ] https://www.youtube.com/watch?v=ltzlhAxJr74

## Talks to Watch
- [ ] [Best practices presentation by Drew Baker - VueJS LA meetup - January 14, 2020 ](https://docs.google.com/presentation/d/1xMqvylzoIwpEgwFEpXI8it_HGo7BUGrt8h65E0nvEQo/edit?usp=sharing)

## Important Concepts (Review)
1.  We care about Chrome, Safari and Firefox in that order.
1.  Don’t leave behind old code.
- [ ] [Max-width](https://www.google.com/search?q=max-width&rlz=1C5CHFA_enUS818US818&oq=Max-width&aqs=chrome.0.0l10.482j0j1&sourceid=chrome&ie=UTF-8)  
    + You can write breakpoints without needing a media query generally.
    + Often using `width` and `max-width` is enough. 
    + Good break points can often be created by using `font-size` and reducing columns.
- [ ] [Collapsible margins](https://www.google.com/search?q=collapsible+margins&rlz=1C5CHFA_enUS818US818&oq=Collapsible+margins&aqs=chrome.0.35i39j0i10l4j0j0i390l4.707j0j1&sourceid=chrome&ie=UTF-8)
- [ ] [Intrinsic ratio sizing](https://www.google.com/search?q=Intrinsic+ratio+sizing&rlz=1C5CHFA_enUS818US818&oq=Intrinsic+ratio+sizing&aqs=chrome..69i57j69i59.975j0j1&sourceid=chrome&ie=UTF-8)
- [ ] Understand when to use 
    + `v-text` sets the textContent of the node. `v-html` sets the innerHTML of the element. `&amp;` is an HTML entity. If you want HTML entities interpreted and replaced, you need to have them interpreted as HTML and not text. Interpreting user's input as HTML poses a security risk.
    - [ ] [`wp-content`]()
    - [ ] [`v-html`](https://www.google.com/search?q=v-html&rlz=1C5CHFA_enUS818US818&oq=v-html&aqs=chrome..69i57j0l9.4668j0j1&sourceid=chrome&ie=UTF-8)
    - [ ] [`v-text`]()

## Basics
1.  No CSS resets
1.  Be semantic - call things what they are. Name your component what the filename is, and give it a class that matches.
1.  In Vue templates, use components like `<component-name/>` not like `<ComponentName>`.
1.  Avoid use of element name selectors in CSS. Don't use `h2`, give it a `.title` class instead.
1.  In general avoid use of CSS pseudo elements like `:content`, `:before`, `:after`. Except for list bullets or underlines.
1.  No use of floats
1.  Don’t use `#` ID’s unless using for JS selectors or actually need page anchors.
1.  Use a central `z-index` location for major structural components, increment by 100’s
1.  For component level `z-index` set top level to 0 and increment by 10
1.  Use positioning sparingly. In general most people over use `position:absolute`.
1.  If using useless markup to get a desired style, you’re doing it wrong. For example wrapping divs, centering divs.
1.  Define CSS for active and hover states at the end of component, followed by breakpoints at end of file please!
1.  When using SCSS if you’re going more than 2 levels deep, question yourself. 
    + Think of the top level element class as a namespace, so things in it don’t need namespaces too.
1.  Never use background-images, use object-fit with src-set instead.
1.  For class names use is-{state} and has-{feature} or not-{type}. Like is-active, is-opened, has-video, not-case-study, is-active.
1.  Common element class names: `block`, `grid`, `panel`, `menu`, `overlay`, `meta`, `title`, `section`, `section-title`.
1.  Margin top/bottom, Padding left/right.
1.  [Use lodash](https://lodash.com/) Instead of using map() and filter() in inventive ways.
1.  Don’t fight the browser - scroll, events, URLs et cetera.
1.  With `Nuxt-Link` or `Router-Link` use relative paths from the root (start with a `/`).
1.  Use white spacing in your templates.
1.  Order your CSS in the same order your markup is in. Top to bottom as coded.
1.  A `switch` statement is better than a lot of `if-else` conditions
1.  [This is how you do forms in Vue.](https://alligator.io/vuejs/vue-form-handling/)
1.  Don't use icon fonts, use SVGs. [SVGO](https://github.com/svg/svgo) is a good tool for optimizing SVGs.
1.  If your component accesses `$store` or `$route` directly, you're doing it wrong. Use props and events instead. 
- [ ]  100vh doesn't work great on mobile. [See this for how to do it right](https://stackoverflow.com/questions/58886797/how-to-access-the-real-100vh-on-ios-in-css).
- [ ] Be sure to include the [`viewBox` attribute](https://www.google.com/search?q=viewBox+attribute&rlz=1C5CHFA_enUS818US818&sxsrf=ALeKk00gO9BELT3J_3f6UrRdo6-PVTA7KQ%3A1618689197170&ei=rTx7YKnpCZLv-gTw8LDgDg&oq=viewBox+attribute&gs_lcp=Cgdnd3Mtd2l6EAMyAggAMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeOgYIABAFEB46BggAEAgQHlDg1wpY0f8KYMCaC2gAcAJ4AIABuwGIAdMEkgEDMy4ymAEAoAECoAEBqgEHZ3dzLXdpesABAQ&sclient=gws-wiz&ved=0ahUKEwjp8-SUh4bwAhWSt54KHXA4DOwQ4dUDCA8&uact=5).
- [ ] This is [a good clean sample](https://github.com/funkhaus/factory/blob/master/src/components/WorkBlock/BlockWork.vue) component to study.

## Be better at
1.  Drew to show everyone how to build top-panel/bottom-panel style fixed sliding sites
1.  Really think hard about what can be a component. Makes a site so hard if you don’t use components.
1.  Know what components and tools.js we have in [fuxt](https://github.com/funkhaus/fuxt) and our [haus components](https://github.com/funkhaus/components)!
1.  Don’t do things rough with the expectation of coming back to it. Do it right the first time, think it through.
1.  Add head() data for SEO as you build each pages. Sucks to do this at the end.
1.  Learn how to spot red flags. Long file? Deep nested CSS? Watching a lot of things? Lots of specific break points? Committing to the store a lot?
1.  Organize your windows into panels of editor and browser and dev tools.
1.  Use Prettier along with the linting tools built into [fuxt](https://github.com/funkhaus/fuxt).
