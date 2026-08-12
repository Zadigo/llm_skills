---
name: expand

description: Expand a problematic statement in a list of arguments that can be used in a debate

hint: "problematic statement" the argument to expand
---
# Expansion guide

## Overview

Expland a problematic statement into a list of arguments that can be used in a debate.

---

## Workflow

### Phase 1: Contextualize the expansion

Analyze the problematic statement and ensure that there is a `geographic` context and a `timeframe`. If none are present, warn the user that it might be extremely general which can lead to certain logical fallacies due to the extremely large sample size.

* Geographic context can be a city, a country or any specific location.
* A timeframe can be a date, a year or a range of anything that composes a date.

Ask the user to provide these elements if they are not present.

### Phase 2: Sketching the arguments

#### Phase 2.1: Determine the scopes of the arguments

Ask the user whether they want to stay strictly within the theme of the problematic statement or whether they would like to get arguments for different concepts of their choice. For instance, if the concept is "sports" and the theme is "fashion style in basketball", they can either stay in theme or want to find arguments for "economics + fashion in sports", "history + fashion style" etc.

#### Phase 2.2: Write ten arguments

Sketch ten first arguments and propose them to the user. Work continuously with them until they are satisfied with the arguments that want to use. Ensure that each arguments respects **strictly** the geographical and timeframe context of the problematic statement.

### Phase 3: Select the sources

Once the arguments are selected the user, select a source for each of them. Check the list of sources provided by the user in `DATA_DIR/sources.csv`. If there are no sources available available, get 2 or 3 sources in your knowledge base that can proove the argument and then ask the user to provide a set of sources.

If he provides sources, read the sources and save their names and description in `DATA_DIR/sources.csv` and their authors in `DATA_DIR/authors.csv`.

#### Phase 4: Write a summary

For each arguments, use the template below to reference the argument to their examples.

```Markdown

# Argument n°1 : [argument title]

- **Observation, proposition, affirmation:** [observation]
- **Examples or proofs:** [proofs]
```

**Argument title**

The rought summarized text of the argument

**Observation**

The obervation or assertion for the argument. The template below can be used to structure the content for the observation and proofs for the user:

```Markdown
Observation: "Investiments in New-York city tend to improve the lifestyle of the people living in the city
Examples or proofs: [link word: indeed, in this respect...] a study published on XYZ shows that ABC
```

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
