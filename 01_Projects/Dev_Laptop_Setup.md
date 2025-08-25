---
Status: Started
Links: "[[🚧 My Projects]]"
tags:
  - project
Deadline: 2025-08-30
Area: "[[A_Software_Engineering]]"
---
## Goal

Setup Dev Laptop and Dev Env

## Motivation

Pop OS is falling short

## Description

Setup dev environment in gpu laptop.

## Related Areas

```dataview
list
From #area and !"Templates"
```

## Notes

- ### Install Ubuntu 25.04

Choose Ubuntu 25.04 because it mentioned compatibility with recent hardware.
Pop Os had issues with rtx card and random freezes.
Touch pad had responsive issues.

Used Ventoy to create boot usb. Just added iso. No issues

Hardware got detected after setup.
Latest nvidia driver work outside the box.
Touch pad detected outside the box.

- ### Install homebrew

Followed steps from [homebrew](https://brew.sh/)
**NOTE:** installed for bash. When installed for zsh, need to point to zsh.

- Install uv

```bash
brew install uv
```


- ### Install Docker

Tried installing docker from brew. Couldn't make it run.
Tried the convenience script. Worked, but did not like it.
Followed [apt method](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)

Docker-compose needs to be installed from apt

```bash
sudo apt update
sudo apt install docker-compose
```

Also added the post installation steps.

- ### Install VS Code

Followed [vscode](https://code.visualstudio.com/docs/setup/linux#_install-vs-code-on-linux) instructions

Have issue creating 