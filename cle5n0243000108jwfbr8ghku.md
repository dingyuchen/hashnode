---
title: "Building a Custom Digital Garden🌲"
datePublished: Wed Feb 15 2023 12:16:03 GMT+0000 (Coordinated Universal Time)
cuid: cle5n0243000108jwfbr8ghku
slug: building-a-custom-digital-garden
tags: blogging, nextjs, digital-garden, pkm

---

2023 is the year I decided to start working on my branding and website.

One of the things that I wanted to do was to make taking notes a more fun and conscious process. I have used many PKM systems in the past, but they never quite hit the spot for me.

Some of the things that I was looking out for were:

* Zettelkasten style notes with bidirectional linking
    
* \\(\LaTeX\\) support
    
* First-class support for publishing (I would like to write my notes to convey ideas to others, not just some personal encoding of information)
    
* A Vim editor
    

To be fair, Dendron was almost exactly what I was looking for, but I did not like its embedding functionality and syntax. Additionally, I wanted to be able to create custom interactive components and insert them in the middle of the page, which means that I will need to write my notes in MDX, which most PKMs do not support.

Another major gripe was not having a semantic overview of my notes. Almost all PKMs, digital gardens, etc., display notes on a single page, or present them in a stack. I feel that this format does not make full use of the *Graph model*, which can show the actual relationship between the pages, yet at the same time, the traditional graph view reduces a page into a node, with no presentation of its contents.

## The Plan

This year, I decided to build my own and integrate it into my personal website.

The idea is to write notes or ideas in MDX, and map them onto their own `React` components using NextJS. There will be a route on my website where anyone can search and place the notes onto an adjustable grid (something like Notion). The notes themselves will be fully browseable in their own cards. If there is a link between 2 notes, a thin line will be rendered between the cards. The user can also create a new link between cards manually.

![Rough sketch of idea](https://cdn.hashnode.com/res/hashnode/image/upload/v1676457730488/d5a639d2-575d-4c9c-bab9-15276c9b6031.jpeg align="center")

It is also a scratchpad to write more notes that reference the organisation of the selected cards. I call this the *Playground View*.

## Snags

Unfortunately, I haven't figured out all the technical details yet. A big one is exporting the playground into an MDX file that I can commit to the repo itself. Using a database is a solution, but it is much less portable. A local-first solution is much preferable.

Another difficulty I foresee would be generating the links and linking between notes. using `wikilinks` is one solution, but I've only seen people using regex to search for occurrences of `[[` to generate links. Ideally, we would also want links to be transformed into a `next/link` component.

Writing notes for my personal website in this way also means giving up all the niceties of the WYSIWYG editors and completions. However, I intend to adopt more of a conscious note-taking process rather than an efficient one. By putting in the manual effort to curate my digital garden, I hope to be able to improve my understanding and expression of the idea I'm writing about.

# Next Steps

I think writing MDX and incorporating interactive React components into my notes would be a good way to improve understanding and perhaps also build a habit of collecting notes. I have managed to integrate MDX pages into my NextJS application, most notably Image Optimization, as I intend to, and benefit greatly from, drawing to express thoughts.

The next thing to do is to set up wikilinks or some form of linking to get inter-note relationships working. Follow along as I get things working! (There will probably be more code for the next post)