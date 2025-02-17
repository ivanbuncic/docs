---
# NOTE: This file is auto-generated from 'scripts/error-docgen.mjs'
# Do not make edits to it directly, they will be overwritten.
# Instead, change this file: https://github.com/withastro/astro/blob/main/packages/astro/src/core/errors/errors-data.ts
# Translators, please remove this note and the <DontEditWarning/> component.

layout: ~/layouts/MainLayout.astro
title: Invalid value returned by a getStaticPaths path.
i18nReady: true
githubURL: https://github.com/withastro/astro/blob/main/packages/astro/src/core/errors/errors-data.ts
setup: |
  import DontEditWarning from '../../../../components/DontEditWarning.astro';
---

<DontEditWarning />


> **InvalidGetStaticPathParam**: Invalid params given to `getStaticPaths` path. Expected an `object`, got `PARAM_TYPE` (E03010)

## What went wrong?
The `params` property in `getStaticPaths`'s return value (an array of objects) should also be an object.

```astro title="pages/blog/[id].astro"
---
export async function getStaticPaths() {
	return [
		{ params: { slug: "blog" } },
		{ params: { slug: "about" } }
	];
}
---
```

**See Also:**
-  [`getStaticPaths()`](/en/reference/api-reference/#getstaticpaths)
-  [`params`](/en/reference/api-reference/#params)


