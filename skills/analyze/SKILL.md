---
name: analyze
description: Analyze an article or document and provide an analysis of the content
---
# Analysis guide

## Overview

Analyze the core structure of an article or a discourse by dissecting the content into its main logical components.

---

## Workflow

### Phase 1: Get the content

Ask the user to upload a file or content that contains the article or discourse to analyze if there is none.

Before analyzing the file, ask the user to briefly describe the type of the content. After this question you should know either if the content is either an `article` or `argument`. Ask the user whether article is part of a dissertation, a scientific article, a news article or any other type of content.

### Phase 2: Choose between article and argument workflow

if the content is an article, resolve the [/srcripts/article](./scripts/article) otherwise, if it's an argument, resolve [/scripts/argument](./scripts/argument).

---

## Permissions Required

Add to `~/.claude/settings.json`:

```json
{
  "permissions": {
    "analyze": {
      "description": "Analyze an article or document and provide an analysis of the content",
      "access": "read"
    }
  }
}
```
