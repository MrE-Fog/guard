---
title: Release | Guard
description: Guard Release
menu:
  product_guard_{{ .version }}:
    identifier: release
    name: Release Process
    parent: developer-guide
    weight: 15
product_name: guard
menu_name: product_guard_{{ .version }}
section_menu_id: setup
---

# Release Process

The following steps must be done from a Linux x64 bit machine.

- Do a global replacement of tags so that docs point to the next release.
- Push changes to the `release-x` branch and apply new tag.
- Push all the changes to remote repo.
- Build and push guard docker image:

```console
cd ~/go/src/go.kubeguard.dev/guard
./hack/release.sh
```

- Now, update the release notes in Github. See previous release notes to get an idea what to include there.
