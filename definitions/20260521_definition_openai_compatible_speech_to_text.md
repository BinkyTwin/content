---
title: 'OpenAI-Compatible Speech-to-Text'
description: 'A speech transcription API shape that accepts OpenAI-style audio transcription requests while routing them to another provider.'
date: 2026-05-21
author: 'Binky Twin'
---

# OpenAI-Compatible Speech-to-Text

## Definition

OpenAI-compatible speech-to-text is an API pattern where a provider accepts
requests shaped like OpenAI audio transcription calls, usually multipart uploads
with a `file`, `model`, optional `language`, and optional prompt or output
format parameters.

## Context and Usage

This compatibility layer lets developers switch transcription providers without
rewriting their entire workflow. A tool can keep one request-building path, then
change credentials, endpoint URL, and model name through environment variables.
It is especially useful in reproducible workspaces where the same command should
run against several providers for cost, latency, or availability comparisons.
