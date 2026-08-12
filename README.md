d

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
| Expand               | `/plato:expand`    | Expand a problematic statemtent to a list of usable arguments                              |

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
claude plugin marketplace add https://github.com/Zadigo/plato-the-lawyer-skills.git

# 2. Install the plugin
claude plugin install zadigo@plato-the-lawyer

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
│       └── ...   
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
├── debating-profile.md                 # The debatting profile of the user
├── authors.csv                         # List of authors
├── sources.csv                			# List of sources
└── topics/                               # One folder per application
    ├── topic-name-2026-02-11/
    │   ├── posting.md                  # Saved job description
    │   ├── resume.md                   # Tailored resume
    │   ├── cover-letter.md             # Cover letter
    │   └── applied.md                  # Application log (date, ATS, status)
    └── ...
```
