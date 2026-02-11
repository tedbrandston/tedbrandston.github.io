---
title: "SLP prefix generator"
originallyWritten: 2026-02-09T17:00:00
tags: [tools, ai]
draft: false
---

I'm generally suspicious of the gen-AI hype, but also curious about how this'll all go. 

The other day Kat tried to generate some lists of words with certain prefixes by asking an AI chatbot. It made up words like "unpossible" because LLMs don't actually understand how words are spelled (see, for example, all the odd answers to "how many Rs in 'strawberry'").

But what if we ask the AI to make a tool that generates the thing we want? The risk if it's wrong is fairly low, and after the initial generation we stop using the AI (and all the energy that goes into running it).

<!--more-->

I gave Gemini 3 Pro the prompt:

> I'd like to make a tool for an SLP to generate word lists for given prefixes. This should be a single-page html+js utility.

> The words can be pulled from wiktionary, e.g., https://en.wiktionary.org/wiki/Category:English_terms_prefixed_with_un-_(negative), and if there are multiple meanings of the prefix they should be able to choose which meaning (so from https://en.wiktionary.org/wiki/un- they should also be able to choose un- (negative), un- (reversive), etc.) from a dropdown, where each item in the dropdown shows how many words there are in that category.
>
> words should be listed in frequency order (is there a free API you can use for that?), ideally with a numeric indicator of frequency.

The first page it produced didn't work, but I gave it a screenshot and said that it wasn't working, and the second try seems to work just fine.

The result is here: [Prefix List Generator](/slp-prefix-gen.html)

EDIT: I also asked it to fix a bug where capitalization messes things up.  
EDIT2: I've also created a tool for finding multiple prefixes with the same root: [Multi-Prefix List Generator](/slp-multi-prefix-gen.html)
