---
layout: distill
title: Can an LLM be tokenizer-free?
description: Your blog post's abstract.
  Please add your abstract or summary here and not in the main body of your text.
  Do not include math/latex or hyperlinks.
date: 2026-04-27
future: true
htmlwidgets: true
hidden: true

# Mermaid diagrams
mermaid:
  enabled: true
  zoomable: true

# Anonymize when submitting
authors:
  - name: Anonymous

# must be the exact same name as your blogpost
bibliography: 2026-04-27-tokenizer-free.bib

# Add a table of contents to your post.
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - please use this format rather than manually creating a markdown table of contents.
toc:
  - name: Can an LLM be tokenizer-free?
  - name: What is Tokenization and Why Does it Exist?
  - name: “Tokenizer-Free” Language Modeling
    subsections:
      - name: The Effects of the Anti-Tokenizer Movement
  - name: In defense of existing tokenization methods
  - name: Citations
  - name: Footnotes

# Below is an example of injecting additional post-specific styles.
# This is used in the 'Layouts' section of this post.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }
---

## Can an LLM be tokenizer-free?

<!-- <d-cite key="gregor2015draw"></d-cite> -->

<!--{% include figure.liquid path="assets/img/2026-04-27-distill-example/iclr.png" class="img-fluid" %} -->

<!--{% twitter https://twitter.com/rubygems/status/518821243320287232 %} -->

<!--> Blockquotes are very handy in email to emulate reply text. -->

The only time most people hear about tokenization is when it’s being blamed for some undesirable behavior of a language model, such as not being able to spell 'strawberry' <d-cite key="silberling2024why"></d-cite>. These incidents have fueled a campaign against tokenizers. This campaign has helped turn ignorance and indifference towards tokenizers into active dismissal and disdain. This makes it harder to understand the tokenizers and develop better ones, because fewer people care about tokenizers and are working to make them better. 

The goal of this blog post is to provide some context about how we got the tokenization approaches we have and argue that they’re not actually so bad. 

On a personal level, I also want to foster more engagement with the tokenization literature.
Regardless of whether you are pro- or anti-tokenization, I want more people to be working on issues related to tokenizers. For one, the more people we have working on it, the faster we’re going to make progress. For those that think they are taking a “tokenizer-free” approach, I argue that these approaches are just other kinds of tokenization. Incorporating the findings from static subword tokenization research can only help develop better alternatives. 
