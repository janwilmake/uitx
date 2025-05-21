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

- cli-based oauth with github
- finds `package.json` and lockfile (for dependencies)
- also finds `git remote` and `context.json` (for repo itself)
- fetches every package context on uithubs api in parallel (authenticated)
- fetches every context on uithubs api in parallel (authenticated)
- writes each result to `/.context`

# ADR

uithub so far has been provided as website where you can browse repos. I started early with https://npmjz.com but this never took off.

[Critics](https://x.com/samgoodwin89/status/1916638156776198340) wanted the context exploration as CLI/library so they can use it at build-time, not dynamically as a service. They have a point!

uitx will provide a new way of accessing your codes context: as a CLI that brings it into any IDE.

Follow along in [this thread](https://x.com/janwilmake/status/1925113500486992375)
