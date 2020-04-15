# Changed Files Action

This GitHub action applies to pull requests and populates 3 output variables with the modified files. They are: "files_created", "files_updated", and "files_deleted".

### Workflow Config Example
```
- name: Changed Files Exporter
  uses: futuratrepadeira/changed-files@v3.1.0
  with:
    repo-token: ${{ github.token }}
    pattern: '^.*\.(md|markdown)$'
```

### Inputs
* **`repo-token`**: GitHub Access Token
* **`pattern`** (optional): A regular expression to filter the outputs by. Defaults to `'.*'`.

### Outputs
All output values are a single JSON encoded array.

* **`files_created`**: Created files
* **`files_updated`**: Updated files
* **`files_deleted`**: Deleted files

