# STRSC Player Log

A lightweight player activity logger for Paper/Spigot servers. It writes daily log files and can post commands and deaths to a Discord webhook. It is a companion to STRSC Staff Core.

**Version:** 1.0.3 | **API:** 1.13+

## What it logs
Joins, quits, kicks, chat, commands, block break/place, deaths, teleports, gamemode changes, item drop/pickup, inventory opens and bucket use. Every event type can be switched on or off in `config.yml`.

## Features
- **Daily log files:** written to `plugins/STRSCPlayerLog/logs/yyyy-MM-dd.log`
- **Discord feed:** commands and deaths go to a webhook of your choice, separate from DiscordSRV chat
- **Privacy:** sensitive commands (`/login`, `/register`, `/changepassword`, `/2fa` and others) are never logged
- **Live reload:** `/playerlog reload` (alias `/plog`)

## Commands and permissions
| Command | Permission | Default |
|---|---|---|
| `/playerlog reload` | `strscplayerlog.reload` | op |

## Installation
1. Drop the jar into `plugins/`.
2. Start the server once to generate `config.yml`.
3. Optional: paste a Discord webhook URL into `discord.webhook-url` and run `/playerlog reload`.

Item pickup logging can be very noisy, so turn it off if your logs grow too fast.

## Soft dependencies
STRSCStaffCore,StaffPlusPlus, AuthMe
