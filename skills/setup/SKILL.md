---
name: setup
description: Onboarding - set preferences
argument-hint: "category" the preferred category for the analysis
tools: Google Drive,Onedrive,Gmail
---
# Setup skill

Onboard the user by setting up his preferences

## Quick start

* `/plato:setup`
* `/plato:setup category`

## File structure

```

scripts/
	conduct_interview.md # Debating style interview guide
```

## Data directory

Resolve the data directory using `shared/references/data-directory.md`. If no directory exists this is a fresh install — create it in Step 1.

## Workflow

### Step 1: Check existing preferences

Resolve the data directory, then check if these files exist: .

If everything exists, tell the user they're good to go and list the available skills. Otherwise, run only the missing phases in order.

### Step 2 : Set preferences

Ask the user in one natural question:

> "What kind of articles are you looking to analyze? Tell me about the preferred categories, and anything you'd want to filter out."

From the response, save `DATA_DIR/preferences.md`:

```markdown
# User Preferences

## Preferred Categories
- [parsed from response]
```

If they leave something out, that's fine — save what you have. They can always update later.

### Step 3: Authors (Optionnal)

If the user wants to add authors, ask them to provide a list of authors they want to add in order to enrich the analysis. Save it in `DATA_DIR/authors.csv`.

The user may upload a CSV file or paste a list of authors. The file can contain: full name, website (optional).

### Step 4: Sources (Optionnal)

If the user wants to add sources, ask them to provide a list of sources they want to add in order to enrich the analysis. Save it in `DATA_DIR/sources.csv`.

The user may upload a CSV file or paste a list of sources. The file can contain: name, author, url (optional).

If the user uploads a list of sources, get the authors column and update the `DATA_DIR/authors.csv` file with any new authors that are not already in the file.

### Step 5: Debating profile (optional)

Ask the user about their debating profile, including

nesses, and preferred debate topics. Save it in `DATA_DIR/debating_profile.md`.

Have a conversational style and if the anwsers are vague or too short, ask follow-up questions to get more details. The goal is to have a comprehensive profile that can be used to tailor the analysis and counterpoints.

For each of the user's preferred categories, ask:

1. What made you interested in this category?
2. What are your strengths in this category?
3. What are your weaknesses in this category?
4. What are your preferred debate topics in this category?

For the fourth question, drill down to a specific sub-category but that is general enough to be applicable to a wide range of articles. For example, if the category is "Politics", ask about specific topics like "Climate Change", "Healthcare", or "Immigration".

After the interview, save the profile to `DATA_DIR/debating_profile.md` in a structured format, such as:

```markdown
# Debating Profile

## Category 1: [Category Name]
- Strengths: [parsed from response]
- Weaknesses: [parsed from response]
- Preferred Debate Topics: [parsed from response]
```

### Step 6: Summary

After all the steps are completed, summarize the user's preferences and profile.

```markdown
You're all set! Here's a summary of your preferences and profile:

- Preferred Categories: [number] of categories added
- Authors: [number] of authors added
- Sources: [number] of sources added

You're read to use:
 
- /plato:analyze
- /plato:counter
- /plato:discourse
- /plato:sources
- /plato:authors
```

---

Add to `~/.claude/settings.json`:

```json
{
  "permissions": {
    "allow": [
      "Read(~/.proficiently/**)",
      "Write(~/.proficiently/**)",
      "Edit(~/.proficiently/**)"
    ]
  }
}
```
