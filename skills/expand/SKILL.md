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

Analyze the problematic statement and ensure that there is a `geographic` context and a `space-time`. If none are present, warn the user that it might be extremely general which can lead to certain logical fallacies due to the extremely large sample size.

* Geographic context can be a city, a country or any specific location.
* A space-time can be a date, a year or a range of anything that composes a date.

Ask the user to provide these elements if they are not present.

### Phase 2: Sketching the arguments

#### Phase 2.1: Determine the scopes of the arguments

Ask the user whether they want to stay strictly within the theme of the problematic statement or whether they would like to get arguments for different concepts of their choice. For instance, if the concept is "sports" and the theme is "fashion style in basketball", they can either stay in theme or want to find arguments for "economics + fashion in sports", "history + fashion style" etc.

#### Phase 2.2: Write ten arguments

Sketch ten first arguments and propose them to the user. Work continuously with them until they are satisfied with the arguments that want to use. Ensure that each arguments respects **strictly** the geographical and space-time context of the problematic statement.

### Phase 3: Select the sources

Once the arguments are selected by the user, select a source for each of them. Check the list of sources provided by the user in `DATA_DIR/sources.csv`. If there are no sources available, get 2 or 3 sources in your knowledge base that can proove the argument and then ask the user if they wish to provide a set of additional sources.

If he provides sources, read the sources and save their names and description in `DATA_DIR/sources.csv` and their authors in `DATA_DIR/authors.csv`.

There might be a case where you might not find any sources on your own that corroborates the claim. In that case, devaluate the argument and warn the user that there might not be any sources for that claim. Ask them to provide credible documents that *strictly* and *directly* support the claim ensuring that they respect the geographic and space-time context at all times.

You can use the rating system below to rate the sources you find for each argument. The rating is based on how well the source supports the claim.

**Source rating (text)**

* **Strong:** The source directly supports the claim and is credible.
* **Moderate:** The source somewhat supports the claim but may not be directly related or may have some limitations.
* **Weak:** The source does not directly support the claim or is not credible.

**Source rating (1 to 5) (numeric)**

* **Theoretical framework (5 = Paradigm-shifting/Foundational, 1 = Weak/Lacks theory):** Does the source offer a robust conceptual lens for the claim?
* **Source Handling (5 = Original/Archival/Rigorous text analysis, 1 = Hearsay/Derivative):** How deeply does the author engage with primary texts, artifacts, or archives?
* **Interpretive Rigor (5 = Nuanced, highly persuasive argument, 1 = Superficial/Polemical):** Is the critique logical, well-supported, and open to historical complexity?
* **Academic Authority (5 = University press/Top-tier peer-reviewed journal, 1 = Self-published/Blog):** Who published the work, and how widely is it cited in the field?
* **Historical Contextualization (5 = Masterful grasp of the era/milieu, 1 = Anachronistic/Out of context):** Does it respect the specific historical or cultural context of the subject?

Actionable evaluation tier list

* **Score 21–25 (Essential):** Anchor text. Engage with its arguments closely in your literature review.
* **Score 15–20 (Supporting):** Secondary critique. Provides useful historical context, counter-arguments, or niche data points.
* **Score Under 15 (Low Priority):** General overview. Skip or use only for minor introductory background.

#### Phase 4: Write a summary

For each arguments, use the template below to reference the argument to their examples. Classify each claim by how strong they are supported by their respective sources. Strongly suggest the user to remove the claims that are unsupported or suggest that he provides strong sources that would improve their ranking.

```Markdown

# Argument n°1 : [argument title] - [total source rating numeric] ([source strength: essentual, supporting, low priority])

- **Observation, proposition, affirmation:** [observation]
- **Examples or proofs:** [proofs]
```

**Argument title**

The rough summarized text of the argument

**Observation**

The obervation or assertion for the argument. The template below can be used to structure the content for the observation and proofs for the user:

```Markdown
Observation: "Investments in New-York city tend to improve the lifestyle of the people living in the city"
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
