> :information_source: `svelte-v4-i18n` is just a dependecies-upgraded version of the original [`svelte-i18n`](https://www.npmjs.com/package/svelte-i18n) package to support svelte >= `4.0.0`.

[![npm version](https://badge.fury.io/js/svelte-v4-i18n.svg)](https://badge.fury.io/js/svelte-v4-i18n)

# svelte-v4-i18n

> Internationalization for Svelte.

`svelte-v4-i18n` helps you localize your app using the reactive tools Svelte provides. By using [stores](https://svelte.dev/docs#svelte_store) to keep track of the current `locale`, `dictionary` of messages and to `format` messages, we keep everything neat, in sync and easy to use on your svelte files.

**Usage**

- **IMPORTANT:** The import has been changed from the original package from `svelte-i18n` to `svelte-v4-i18n`

```svelte
<script>
  import { _ } from 'svelte-v4-i18n'
</script>

<h1>{$_('page.home.title')}</h1>

<nav>
  <a>{$_('page.home.nav', { default: 'Home' })}</a>
  <a>{$_('page.about.nav', { default: 'About' })}</a>
  <a>{$_('page.contact.nav', { default: 'Contact' })}</a>
</nav>
```

```jsonc
// en.json
{
  "page": {
    "home": {
      "title": "Homepage",
      "nav": "Home"
    },
    "about": {
      "title": "About",
      "nav": "About"
    },
    "contact": {
      "title": "Contact",
      "nav": "Contact Us"
    }
  }
}
```

**Requirements**

- Node: `>= 16.0.0`
- Browsers: `Chrome 38+`, `Edge 16+`, `Firefox 13+`, `Opera 25+`, `Safari 8+`.

- [Documentation / Getting Started](/docs/Getting%20Started.md)
- [Usage with Svelte Kit](/docs/Svelte-Kit.md)
- [i18n VSCode extension (3rd party)](https://github.com/antfu/i18n-ally)
