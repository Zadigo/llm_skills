# Plato The Lawyer

**Plato the lawyer** is Claude plugin that allows the user to analyse a discourse by referencing the different biases and logical fallacies within it.

## Skiils

| Skill                | Command              | Quick description                                                                          |
| -------------------- | -------------------- | ------------------------------------------------------------------------------------------ |
| Setup                | `/plato:setup`     | On-boards the user by setting up the preferences for the plugin                            |
| Analyze              | `/plato:analyze`   | Analyze a discourse or an article                                                          |
| Create counter point | `/plato:counter`   | After analyzing an article write a simple counterpoint using the user's preferred sources |
| Create discourse     | `/plato:discourse` | After analyzing an article write a discourse                                               |
| Get sources          | `/plato:sources`   | List the sources preferred by the user                                                     |

## Installation

### Using Claude Co-work

* Download [Claude Cowork](https://claude.com/product/cowork) (if you haven't already)
* Download the plugin as a zip from GitHub
* In Cowork, go to **Plugins** (left sidebar) and click the **+** button
* Select **Upload plugin**
* Drag and drop the downloaded zip file, then click **Upload**
* Run `/plato:setup` to get started

### Using Claude CLI

```Shell

# 1. Add the repository as a marketplace
claude plugin marketplace add https://github.com/Zadigo/proficiently-claude-skills.git

# 2. Install the plugin
claude plugin install proficiently@proficiently

# 3. Run setup
/plato:setup
```

## File structure

**Plugin installed via the marketplace**

```
plato/
├── .claude-plugin/
│   └── plugin.json                     # Plugin manifest
├── shared/
│   ├── templates/
│   │   └── profile.md                  # Work history profile template
│   └── references/
│       ├── data-directory.md           # Data directory resolution algorithm
│       └── priority-hierarchy.md       # Instruction priority hierarchy
├── skills/
│   ├── analyze/
│   │   ├── SKILL.md
│   │   └── scripts/
│   ├── setup/
│   │   ├── SKILL.md
│   │   ├── assets/templates/
│   │   └── scripts/
│   └── jobsearch-telegram/
│       └── SKILL.md
└── README.md
```

**User data created by setup**

```
`~/.plato/
├── resume/                             # Your resume PDF/DOCX
├── profile.md                          # Work history from interview
├── preferences.md                      # Job matching rules
├── application-data.md                # Reusable form field answers
└── jobs/                               # One folder per application
    ├── google-lead-gpm-2026-02-11/
    │   ├── posting.md                  # Saved job description
    │   ├── resume.md                   # Tailored resume
    │   ├── cover-letter.md             # Cover letter
    │   └── applied.md                  # Application log (date, ATS, status)
    └── ...
```
