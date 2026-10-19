---
title: Claude Humanizer Skill
version: 1.0.0
author: yousafmohammad762-coder
license: MIT
description: |
  A small skill that rewrites AI model output to read like natural human-written text while preserving meaning and factual accuracy.
tags:
  - humanizer
  - anthopic
  - claude
  - prompt-engineering
  - post-processing
---

# Claude Humanizer Skill

This repository contains a "humanizer" skill: a prompt wrapper and light integrations (Python + Node) that take model output and rewrite it to sound more natural, empathetic, concise, or targeted to a specific audience while preserving factual content.

## Purpose

Use this skill as a post-processing step after generating text with Claude/Anthropic (or other models). It rewrites assistant responses to meet tone, formality, length, and reading-level requirements without adding new facts.

## Key files

- README.md — project overview and quick start
- python/claude_humanizer.py — minimal Python example
- node/ — Node + Express middleware sketch
- SKILL.md — this file (metadata + usage)

## Usage (short)

1. Call your language model to produce an initial response.
2. Send the model output (or the surrounding prose) to the humanizer prompt from python/claude_humanizer.py or node middleware with your chosen options (tone, formality, reading level, length).
3. Use the returned rewritten text in your application (support replies, docs, marketing, etc.).

## Prompt metadata

The skill relies on a structured system prompt with parameters for:
- tone: friendly | professional | empathetic | casual | concise
- formality: formal | neutral | informal
- reading_level: e.g., 6th | 8th | 10th | college
- length: short | medium | long
- preserve_formatting: true | false
- safe_mode: true | false

## Licensing

This project is licensed under the MIT License. See LICENSE for details.
