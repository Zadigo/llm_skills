---
name: analyze
description: Analyze an article or document and provide an analysis of the content
allowed-tools: Read, Write, google-drive:read_file_content, dropbox:GetFileContent
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

if the content is an article, resolve the [/scripts/article](./scripts/article.md) otherwise, if it's an argument, resolve [/scripts/argument](./scripts/argument.md).

Consider an article to be a text with multiple paragraphs where as an argument would be one or multiple lines or eventually just a singe paragraph.

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
