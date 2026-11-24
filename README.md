# Love at First Breach 2026 - CTF Write-ups

A collection of challenge walkthroughs and evidence notes from **Love at First Breach 2026**. The write-ups cover practical web application security and AI security topics, including prompt injection, information disclosure, broken access control, JWT validation, and local file inclusion.

> **Spoiler warning:** Individual walkthroughs contain exploit steps and challenge flags. They are intended for the original CTF/lab environments and authorised security learning only.

## Challenge index

| Challenge | Security topics | Walkthrough |
|---|---|---|
| **CupidBot** | AI prompt injection, system-prompt disclosure, hidden data exposure, guardrail bypass | [Challenge notes](./CupidBot/CupidBot.md) · [Summary](./CupidBot/Readme.md) |
| **Hidden Deep Into My Heart** | `robots.txt` information disclosure, hidden admin paths, credential exposure, weak authentication | [Challenge notes](./Hidden%20Deep%20Into%20my%20Heart/Hidden%20Deep%20Into%20my%20Heart.md) · [Summary](./Hidden%20Deep%20Into%20my%20Heart/Readme.md) |
| **Love Letter Locker** | IDOR, broken object-level authorisation, predictable object identifiers | [Challenge notes](./Love%20Letter%20Locker/Love%20Letter%20Locker.md) · [Summary](./Love%20Letter%20Locker/Readme.md) |
| **TryHeartMe** | JWT `alg: none`, token-claim tampering, privilege escalation, business-logic flaws | [Challenge summary](./TryHeartMe/Readme.md) · [Walkthrough](./TryHeartMe/TryHeartMe.md) |
| **Valenfind** | Local file inclusion, path traversal, source disclosure, exposed secrets, broken access control | [Challenge summary](./Valenfind/Readme.md) · [Walkthrough](./Valenfind/Valenfind.md) |

## Learning themes

- **AI application security:** prompt injection and unintended disclosure of hidden instructions or data.
- **Web application security:** authentication versus authorisation, IDOR, and access-control testing.
- **Token security:** JWT signature and algorithm validation, and server-side trust boundaries.
- **Information disclosure:** exposed files, source code, credentials, and administrative functionality.

## Responsible use

These are educational CTF write-ups. Reproduce the techniques only in the challenge instances or other systems where you have explicit permission. Do not use challenge credentials, flags, or exploit steps against unrelated services.