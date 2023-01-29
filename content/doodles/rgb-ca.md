---
title: "RGB Cellular Automata"
tags: []
draft: false
wasm: /wasm-doodles/rgb_ca.wasm
canvasWidth: 600
canvasHeight: 800
---

Based on Cliff Biffle's tremendously cool [rust+webassembly series](https://cliffle.com/blog/bare-metal-wasm/), and [continuing to riff on cellular automata](/doodles/black-and-white-ca/), this uses three states instead of two. The extra state takes us from 2<sup>3</sup> = 8 "parent rules" and 2<sup>8</sup> = [256 rulesets](https://mathworld.wolfram.com/ElementaryCellularAutomaton.html), up to 3<sup>3</sup> = 27 "parent rules" with 3<sup>27</sup> = 7,625,597,484,987 rulesets!

I found that things got, visually, a little muddled with three colors, so I have it start out zoomed in on each one, so you can see the detail and patterns better, and then zoom out as it finishes calculating the image.

I also switched from treating the borders as "background color" to having them wrap horizontally. I think this makes it a little easier to see what's happening on the rulesets that produce horizontal striping.
