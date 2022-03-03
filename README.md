# rehype-ad-vacuum

>  [rehypejs][rehype] + [Easylist](https://easylist.to/) and company

uses :
- https://github.com/syntax-tree/hast-util-select
- https://github.com/syntax-tree/unist-util-select
- https://github.com/syntax-tree/unist-util-remove
- https://github.com/syntax-tree/unist-util-is

## Installing

```js 
// deno world
import rehypeAdVacuum from 'https://denopkg.com/ericdmoore/rehype-ad-vacuum@main/mod.ts'
```

```js
// Yarn | NPM world
// npm i rehype-ad-vacuum
// yarn add rehype-ad-vacuum
// no CJS/ require support
import rehypeAdVacuum from 'rehype-ad-vacuum'
```

## Usage

```ts 
// deno world
import { unified } from 'https://denopkg.com/ericdmoore/unified@main/mod.ts';
import rehypeParse from 'https://denopkg.com/ericdmoore/unified@main/mod.ts';
import {vacuum, starterLists} from 'https://denopkg.com/ericdmoore/rehype-ad-vacuum@main/mod.ts'

const someCoolUrl:string = await getRandUrlFromDB()
const html = await (await fetch(someCoolUrl)).text()

unified().
.use(rehypeParse)
.use(rehypeAdVacuum, {lists: starterLists})
.process(html)
```

```ts
interface ABPRuleInit {
    protocol?: string;
    username?: string;
    password?: string;
    hostname?: string;
    port?: string;
    pathname?: string;
    search?: string;
    hash?: string;
    baseURL?: string;
    elementBy:{
        allow?: boolean
        selector?: string
    }
} // type is basically {URLPattern & {elementBy}}
```
<!-- Definitions -->
[rehype]: https://github.com/rehypejs/rehype
