# Security Policy

## Maintainer

Elite Holograms is maintained by [EliteScouter](https://github.com/EliteScouter), who is the project's owner and its security maintainer. Every security report is received, triaged and fixed by the maintainer, and every release is built and published by the maintainer.

## Supported Versions

Security fixes are made on the latest release of each edition. Older releases do not receive fixes, so please update before reporting.

| Edition | Minecraft | Loader | Supported version |
| ------- | --------- | ------ | ----------------- |
| `forge19` | 1.19.2 | Forge | `1.19.2-1.3.0` |
| `forge20` | 1.20.1 | Forge | `1.20.1-1.3.0` |
| `fabric20` | 1.20.1 | Fabric | `1.20.1-1.3.1` |
| `fabric21` | 1.21.1 | Fabric | `1.21.1-1.3.0` |
| `neo21` | 1.21.1 | NeoForge | `1.21.1-1.3.0` |
| `neo26` | 26.1.2 | NeoForge | `26.1.2-1.3.0` |
| `neo262` | 26.2 | NeoForge | `26.2-1.3.0` |

Only builds downloaded from the official [Modrinth](https://modrinth.com/mod/elite-holograms) and [CurseForge](https://www.curseforge.com/minecraft/mc-mods/elite-holograms) pages or built from this repository are supported. A jar from anywhere else may have been modified.

## Reporting a Vulnerability

**Please do not report security issues in public issues, pull requests, Discord or comments.**

Report privately through GitHub instead:

1. Open the [Security tab](https://github.com/EliteScouter/EliteHolograms/security) of this repository
2. Click **Report a vulnerability**
3. Fill in the form. Only the maintainer can see it

Please include:

* The edition and mod version, and the Minecraft and loader versions
* Which permission mod is installed, if any (LuckPerms, FTB Ranks, or none)
* What an attacker can do, and what access they need to do it (any player, a player with certain permissions, an operator, or someone with file access)
* Steps to reproduce, ideally on a fresh server with only Elite Holograms and its dependencies installed

## What to Expect

* An acknowledgement within 3 days
* An assessment within 7 days, saying whether the report is accepted and how serious it is
* For accepted reports, a fix released for every affected edition, usually within 30 days. Critical issues are handled first
* Updates as the fix progresses, and a chance to check the fix before it is released

Once a fix is released, the issue is published as a GitHub security advisory and noted in the [changelog](CHANGELOG.md). Reporters are credited unless they ask not to be. Please keep the details private until the fix is out.

## Scope

Elite Holograms is a server side mod, so the issues that matter most are those a player can trigger from the game. Examples of what is in scope:

* Running a command, or an action, that should require a permission the player does not have
* Clickable holograms running commands with more authority than intended, or being triggered by a player they should not respond to
* Text, placeholders or names that let a player inject commands, formatting or click events into what other players see
* Crashing or freezing the server, or flooding clients, through commands, holograms or packets
* Reading or writing files outside the mod's config directory
* Losing or corrupting saved holograms and scoreboards through something a player can do

Out of scope:

* Anything that needs operator status, console access or write access to the server's files, since those already grant full control of the server
* Problems in Minecraft, Forge, NeoForge, Fabric, Fabric API or a permission mod, which should be reported to that project. If Elite Holograms makes such a problem worse, that part is in scope
* Builds that were modified, or downloaded from an unofficial source
* Releases that are no longer supported

If you are not sure whether something is in scope, report it privately anyway.
