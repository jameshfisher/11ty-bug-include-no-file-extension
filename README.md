# 11ty bug: `include` does not work with file with no extension 

Steps to reproduce:

```
npm install
npx eleventy
```

Expected behavior: successful build

Actual behavior:

```
$ npx eleventy
Problem writing Eleventy templates: (more in DEBUG output)
> Having trouble rendering liquid (and markdown) template ./page-about-make.md

`TemplateContentRenderError` was thrown
> ENOENT: Failed to lookup Makefile.liquid in: _includes,., file:./page-about-make.md, line:12

`RenderError` was thrown
> ENOENT: Failed to lookup Makefile.liquid in: _includes,.

`Error` was thrown:
    Error: ENOENT: Failed to lookup Makefile.liquid in: _includes,.
Wrote 0 files in 0.08 seconds (v0.11.1)
```
