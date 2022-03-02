# rehype-ad-vacuum

>  [rehypejs][rehype] + Easylist and company

uses :
- https://github.com/syntax-tree/hast-util-select
- https://github.com/syntax-tree/unist-util-select
- https://github.com/syntax-tree/unist-util-remove
- https://github.com/syntax-tree/unist-util-is

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
