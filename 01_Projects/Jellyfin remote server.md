---
Area:
  - "[[A_Software_Engineering]]"
Status: Started
tags:
  - project
Deadline: 2026-01-09
Links: "[[🚧 My Projects]]"
---
## Goal

- Bael
	- Tailscale accept routes
- Xi
	- re install ubuntu lts
	- tailscale
		- Set up
		- share local net
		- accept routes?
- Penelope
	- re install ubuntu 
	- tailscale
		- Set up
		- share local net
		- accept routes?

## Motivation

- Streaming services suuuuuuuck.
## Description

- Give remote access from Bael - jellyfin server to Xi and Penelope.

## Related Areas

```dataview
list
From #area and !"Templates"
```

## Documentation

Both servers need to have the `accept-routes` flag enabled.
The demo was on mac/windows. So it was enabled by default.
Linux has it disabled by default.

I used tailscale's ip v4 instead of localhost and 127.0.0.1. Not sure if this was necesary or not since the server is in a docker container.

`
```
 sudo tailscale serve --service=svc:jellyfin --https=443 http://100.81.22.110:8096