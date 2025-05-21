# UITX - Context Manager CLI

UITX makes [uit](https://github.com/janwilmake/uit) available for programmatic use and as a CLI.

## Usage:

- As CLI: `npx uitx`
- As script: `npm i --save-dev uitx` and add `{ "scripts": { "context": "uitx" } }` to your package.json
- Programmatically: `npm i uitx` and `import { pipe } from "uitx";`

> [!IMPORTANT]
> Work in Progress

## POC: Focus on CLI

- cli-based oauth with github
- finds `package.json` and lockfile (for dependencies)
- also finds `git remote` and `context.json` (for repo itself)
- fetches every package context on uithubs api in parallel (authenticated)
- fetches every context on uithubs api in parallel (authenticated)
- writes each result to `/.context`

This already provides value by neatly creating a single folder per dependency, plus a folder for your own repo/package that provides improved context

# ADR

uithub so far has been provided as website where you can browse repos. I started early with https://npmjz.com but this never took off.

[Critics](https://x.com/samgoodwin89/status/1916638156776198340) wanted the context exploration as package manager installable library so they can use it without API key in their own projects running the code on their own servers. They have a point!
