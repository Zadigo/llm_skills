# Data directory resolution

All the user's data is stored in `.plato/`folder. In order to find it, you can run the following steps.

## Resolution algorithm

1. Check the current working directory `.plato`
2. Check the following path `~/.plato`
3. If you cannot find either:
   1. It is a fresh setup then create it in step 1
   2. Tell the user to run `/plato:setup` then stop

### Ephemeral session

If not folder in selected (i.e. the working directory) -; a path like `/sessions/...` stop and tell the user:

> "Before we start, you need to select a folder so that your data can persist between sessions. Click "work in a folder" and select your home directory then try again"

Do NOT proceed without a persistent folder.

## DATA_DIR structure

All paths in skill instructions use `DATA_DIR` to mean whichever `.plato/` directory was found or created.

```
DATA_DIR/
    authors.csv # List of authors
    debating-profile.md
    sources.csv
```
