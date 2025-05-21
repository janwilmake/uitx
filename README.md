# UITX - Context Manager CLI

[![janwilmake/uitx context](https://badge.forgithub.com/janwilmake/uitx)](https://uithub.com/janwilmake/uitx) [![](https://badge.xymake.com/janwilmake/status/1925113500486992375)](https://xymake.com/janwilmake/status/1925113500486992375)

UITX makes [uit](https://github.com/janwilmake/uit) available for programmatic use and as a CLI.

## Usage

- As CLI: `npx uitx`
- As script: `npm i --save-dev uitx` and add `{ "scripts": { "context": "uitx" } }` to your package.json
- Programmatically: `npm i uitx` and `import { pipe } from "uitx";`

## POC: Focus on CLI

> [!IMPORTANT]
> This is a **Work in Progress**. This already provides value by neatly creating a single folder per dependency, plus a folder for your own repo/package that provides improved context. It nails the entire flow that's needed to be adoptable in the developers IDE, while keeping things simple, making this a fully API based CLI for now. At a later stage, we can add support for more fine-grained control for which context to build, for example through plugins like `openapi` and `swc` (WIP).

- ✅ cli-based oauth with github
  - ✅ proxy: https://www.lmpify.com/httpsuuithubcom-ow5mjz0
  - ✅ oauth: https://www.lmpify.com/httpsuithubcomj-m8tfk00
- Gathering codebase footprint files
  - Finds `package.json` and lockfile (for dependencies) --> sends that to dependency resolver api (i made before)
  - Also finds `git remote` and `context.json` (for repo itself)
- fetches every package context on uithubs api in parallel (authenticated)
- fetches every context on uithubs api in parallel (authenticated)
- writes each result to `/.context`

# ADR

Follow along in [this thread](https://x.com/janwilmake/status/1925113500486992375) (md version [here](https://xymake.com/janwilmake/status/1925113500486992375))

This is a continous project and I may take breaks at a time. If you want this to exist, don't hesitate to let me know why in the thread.
