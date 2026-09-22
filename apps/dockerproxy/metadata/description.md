# Docker Socket Proxy

## What?
This is a security-enhanced proxy for the Docker Socket.

## Why?
Giving access to your Docker socket could mean giving root access to your host, or even to your whole swarm, but some services require hooking into that socket to react to events, etc. Using this proxy lets you block anything you consider those services should not do.

## Grant or revoke access to certain API sections
You grant and revoke access to certain features of the Docker API through environment variables. Normally the variables match the URL prefix (i.e. AUTH blocks access to /auth/* parts of the API, etc.).

Possible values for these variables:
- 0 to revoke access.
- 1 to grant access.