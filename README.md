# RynxRex Companion

**Your island. Your group. Your next life.**

RynxRex Companion is the Windows desktop companion for the **RynxRex The Isle Evrima community server**. It brings proximity voice, a group map, dinosaur storage, a player marketplace, custom skins and community features into one application.

This is a community project for RynxRex. It is **not an official The Isle application** and is not presented as endorsed by the game's developers.

| Release information | Details |
| --- | --- |
| Current downloadable build documented here | **3.23** |
| Platform | Windows, 64-bit |
| Installer | `RynxRex-Companion-Setup-3.23.exe` |
| Exact installer size | **248,033,557 bytes** — approximately 248 MB / 236.54 MiB |
| Community and support | [Join the RynxRex Discord](https://discord.gg/H5ugndhwAW) |
| Currency used inside the Companion | Server-managed **Points** |

## Contents

- [Download and install](#download-and-install)
- [First launch and account verification](#first-launch-and-account-verification)
- [Features](#features)
- [Security and file verification](#security-and-file-verification)
- [Privacy and permissions](#privacy-and-permissions)
- [Updates and saved settings](#updates-and-saved-settings)
- [Troubleshooting](#troubleshooting)
- [Support and tickets](#support-and-tickets)
- [Release 3.23 notes](#release-323-notes)
- [Important limits](#important-limits)

## Download and install

1. Open the **Releases** section of this GitHub repository.
2. Open the release you want and expand **Assets**.
3. Download **`RynxRex-Companion-Setup-3.23.exe`** for the build described in this document. GitHub's automatically generated **Source code** ZIP/TAR files are not the Windows installer.
4. Check the filename and SHA-256 using the instructions below.
5. Scan the downloaded file with your security software.
6. Run the installer and follow its instructions.
7. Open **RynxRex Companion**, join our Discord and read the server rules.

The packaged player application includes its required runtime components. Players do not need to install Python, Unreal Editor or the Discord bot to use this installer.

The installer is for the **player Companion**, not the game server or host administration panel. Discord tickets and information channels are operated by the separate community bot; players do not install that bot on their computers.

Use releases linked from our official Discord and this repository. Check the repository owner and release address before downloading. A familiar filename alone does not identify a trustworthy file.

## First launch and account verification

1. Join the **RynxRex** server in The Isle Evrima.
2. Type **`!verify`** in the game chat.
3. Copy the private verification code sent to you.
4. In the Companion, choose **Verify account** and enter that code.
5. Wait for the application to confirm the linked account.

**Keep your verification code private.** Do not post it in Discord, screenshots, GitHub issues or public chat. Staff do not need your Steam password, Discord password, Steam Guard codes or Discord bot token to help with verification.

Account linking and voice connection are separate actions. **Verifying your account does not open your microphone.** Open the voice page and explicitly connect when you want to use proximity voice.

After successful verification, the application can remember a revocable device session for this Windows user and the trusted RynxRex server. Closing or updating the application should preserve that remembered link. A different computer, Windows account, revoked session or changed server identity can require verification again.

## Features

### Proximity voice

Talk to nearby players using positional voice based on the live information supplied by the RynxRex game server.

- Select your microphone and output device.
- Configure push-to-talk and supported keyboard/mouse bindings.
- Use voice activation if you prefer it to push-to-talk.
- Adjust volume, activation threshold, Mute and Deafen.
- View voice activity through the optional overlay.
- Reconnect after temporary network interruptions with bounded retry delays.

The microphone stream opens only after an explicit voice connection, authentication and the connection's certificate checks. Once connected, the audio device can remain open for the level meter and activation detection. Audio is transmitted when the selected activation conditions permit it and voice is not muted, deafened or disabled by the server.

When there is no fresh living-character position, voice transmission and reception are automatically suspended. They can resume after a living character and a fresh server position become available. Manual Mute and Deafen settings still apply.

Alt-Tab hides the game overlays but does not by itself disconnect an active voice session. Use Disconnect or close the application when you want to end that session.

### Map Tracker and group minimap

Map Tracker displays your server-supplied position and the available living members of your actual **The Isle group**.

- Ordinary players see their own group members through the group feature.
- Group membership is read by the server; a client cannot choose somebody else's group ID.
- Group markers disappear when membership changes, data expires or the relevant living character is no longer available.
- Use personal map notes such as waypoints, nests, water and danger markers.
- Configure minimap position, size, opacity, zoom and its toggle shortcut.
- Choose reference map layers and named areas.

The compact minimap uses a simplified presentation. The main map provides more room for labels and details. Staff have a separate privileged map/radar capability; it is not an ordinary player's group map permission.

Map terrain and reference geometry may be downloaded to a local cache. The current reference layers include static Gateway area and zone information. **Reference migration/patrol outlines do not prove that a zone is currently active in the game.** Map changes and calibration can affect alignment.

Map Tracker access is controlled by the server. The documented default purchase price is **70,000 Points**; staff or other configured access rules can differ.

### Dinosaur Vault: Store and Load

The Vault is for keeping a server-managed dinosaur snapshot and restoring an eligible stored dinosaur later.

Stored data is intended to preserve the dinosaur's recorded state, including species, sex, growth, Prime information, mutations, colors and supported vital statistics. The exact live result depends on the game's available save/restore fields and successful server confirmation.

Current Store/Load rules include:

- Store requires at least **60% growth**.
- The current Store warmup requires remaining still for **30 seconds** at full health.
- A successful Store removes the live dinosaur and creates its stored record.
- Load requires an eligible fresh character of the **same species and sex**, below **30% growth**.
- A successfully loaded record is consumed and disappears from the available stored inventory.
- A transaction still awaiting confirmation or staff review must not be treated as completed.

Wait for the final server result. Repeatedly pressing Store or Load does not repair an interrupted operation. If a record becomes locked or fails, open a ticket with its dinosaur ID and the approximate time.

Storage slots can be purchased from the Vault. The documented price is **25,000 Points per additional slot**. New accounts start with zero slots; grandfathered accounts retain their existing allocation. The configured capacity can extend up to **20,000 slots per account**. These are storage permissions, not a promise that all slots are rendered on one screen.

### Player dinosaur marketplace

Players can list eligible stored dinosaurs for sale and set a price in the existing Points currency.

Listings expose the recorded information available for the dinosaur, including its species, growth, Prime status, mutations, saved colors and a visual preview. Buyers should inspect these details before confirming a purchase.

A confirmed purchase transfers the stored record to the buyer and credits the seller according to the server transaction. The buyer needs the required Points and a free Vault slot. **Buying a dinosaur does not immediately replace the character you are currently playing.** Restore it through the Vault when eligible.

Saved colors travel with the stored dinosaur. The transfer is of the stored snapshot, not just its name or a generic dinosaur of the same species.

### Custom skins and previews

The skin editor uses the current dinosaur information to prepare the relevant preview and color regions. You can inspect the preview, change regions and submit a completed repaint with **Done**.

- Normal player repainting currently costs **2,000 Points per completed repaint**.
- Staff and Streamer roles have the configured free-repaint benefit.
- Editing and rotating a draft preview does not itself submit a repaint.
- Saved palettes help reuse a design without manually rebuilding each color.
- Applied colors can be captured in a subsequent Store snapshot.

The desktop preview uses game-derived reference geometry and skin masks. Adult reference geometry, default patterns, growth, lighting and species differences can make the final live appearance different from the preview.

Full bright red is reserved for staff on duty. Normal players and Streamers must use non-bright-red colors for **both Flank and Underbelly** under the current server policy. A Streamer role does not grant staff authority.

### Collectible skins, inventory and crafting

The current catalogue contains **90 distinct complete designs**:

| Rarity | Designs | General direction |
| --- | ---: | --- |
| Common | 16 | Restrained, natural-looking combinations |
| Uncommon | 16 | More individual accents |
| Rare | 16 | Stronger separation and contrast |
| Epic | 12 | More expressive combinations |
| Legendary | 10 | Bold premium combinations |
| Mythic | 20 | Distinct designs with animated regional accents |

Inventory supports rarity ordering and management of eligible items, including transfer, sale, deletion and recycling. Recycling produces material according to rarity; eligible material can be used to forge a Mythic. Read the displayed costs and effects before submitting an action.

Current skin uses are designed around a dinosaur's life. Successfully applied one-life skins are intended to remain with the same living dinosaur through Safe Log and server restarts, and to end when that dinosaur dies. Read the item's own usage description for legacy or separately configured items.

Mythic animation in this release uses the game's existing color regions and coordinated accent phases. **It is not a spatial RGB wave moving from feet to head, an emissive shader or a particle aura.** The separate experimental client-mod prototype is not included in this installer.

### Points and optional arcade games

The application uses a server-managed Points balance for supported purchases, market trades and optional games. Daily rewards are one way to earn those Points; they are not a separate currency.

The arcade includes Roll, Crash, Blackjack, Coinflip and Jackpot, alongside crates and collectible inventory. Stakes can be lost. Check the rules, displayed limits and payout information before playing. The current Crash implementation has a configured maximum of **300×**.

**Outcome visibility disclosure:** the current server implementation includes an Owner-only forecast for active Roll and Crash outcomes. These modes should not be described as operator-blind or as an independently audited fair gambling service. A cryptographic commitment does not remove the Owner's configured advance visibility.

### Staff and Owner tools

Privileged actions are authorized by the server's role checks, not merely by whether a button is visible in the client.

Depending on role, tools include Points grants, a staff map, storage review and administration, account role management, and staff-duty colors. Owner storage tools can inspect player inventories and perform supported removal, addition or transfer operations with an audit reason.

The normal player installer does not make a player an administrator. Staff access is a server-side decision.

## Security and file verification

### What has actually been checked

The **specific 3.23 installer identified below** was scanned locally using Microsoft Defender on **29 October 2026, completed at 18:36 Europe/Sofia**. Defender reported:

> Found no threats.

The custom scan completed with exit code **0**. A separate `SECURITY-SCAN.md` accompanies this README with the scope and result. This is a local scan result for this exact file, **not** a claim of independent certification, a VirusTotal report or a guarantee that antivirus software can detect every possible threat.

Release preparation also included isolated installation/uninstallation checks, packaged-source and asset checks, and verification of an in-app update download. Those are useful functional and integrity checks, not an independent security audit or penetration test.

### Exact SHA-256 for build 3.23

Filename:

```text
RynxRex-Companion-Setup-3.23.exe
```

Exact size:

```text
248033557 bytes
```

SHA-256:

```text
24A2D47264B211766CDA73A0F97484B57539D18E1913B9808126EB63559606B2
```

To check your downloaded copy, open PowerShell in the folder containing the installer and run:

```powershell
Get-FileHash -LiteralPath '.\RynxRex-Companion-Setup-3.23.exe' -Algorithm SHA256
```

The result must match the complete hash above. If it does not, do not run that file; re-download it from the official release and contact support if it still differs.

A matching hash shows that two files have identical contents. **It does not by itself prove that a program is harmless**, and it depends on obtaining the expected hash from a trustworthy source. These values apply to 3.23 only; future builds need their own hashes and scan results.

Reference: [Microsoft documentation for Get-FileHash](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/get-filehash).

### Windows signing and SmartScreen

The current 3.23 installer **does not have a Windows Authenticode publisher signature**. Windows can therefore show an unknown-publisher or reputation warning. This README does not claim that a trusted Windows publisher certificate is present.

SmartScreen checks reputation as well as publisher information. An unfamiliar-file warning is not, on its own, a malware diagnosis; it is also not something to dismiss automatically. Verify the download source, hash and security scan before deciding whether to run a file.

**Do not disable Defender, SmartScreen, your firewall or other protections, and do not add blanket antivirus exclusions to install the Companion.** If a security product identifies a specific threat, stop and report the exact detection name, file hash and security-product version to support for investigation.

Reference: [Microsoft's SmartScreen explanation for app developers](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation).

### In-app update protection is a separate mechanism

The application's update system checks:

1. The configured TLS connection and pinned server identity.
2. Signed release metadata using the bundled **Ed25519 public key**.
3. The expected installer size and **SHA-256**.
4. The installer again before the installation handoff.

The Ed25519 update signature is **not** a Windows Authenticode signature and does not create Windows publisher reputation. It protects the update process against untrusted or modified release data within its trust model; it does not replace malware analysis or an independent audit.

The player installer is separate from the host's private configuration. Host databases, Discord bot tokens and private update-signing credentials do not belong in a public release.

## Privacy and permissions

The application needs some access to provide its features. The following explains the intended use rather than asking players to trust an unexplained permission prompt.

| Information or access | Purpose |
| --- | --- |
| Selected microphone | Voice input after explicitly connecting |
| Selected playback device | Nearby voice playback and audio output |
| Keyboard/mouse shortcuts | Push-to-talk, overlay toggles and shortcut binding |
| Linked account identity and server-issued player ID | Account ownership checks, Points and server actions |
| Live game position and group metadata supplied by the server | Proximity voice and permitted group markers |
| Dinosaur snapshot information | Vault operations, marketplace details and skin state |
| Local preferences, notes and cache | Remembered settings, personal map notes and downloaded reference assets |
| Network access | RynxRex services, update checks and map/reference downloads where used |

The described voice path processes audio for live communication; it does not include a voice-recording-to-disk feature. Other participants may independently record their own gameplay or audio, so do not assume voice conversations are impossible to record.

Voice uses the server relay. Transport TLS should not be confused with a claim of end-to-end encryption against the server operator.

The remembered device credential is protected locally with **Windows DPAPI** for the current Windows user and is stored outside the application installation folder. The host stores a hash of the issued device credential. The raw one-time verification code is not the remembered login credential.

Server administrators operate the account, Points, marketplace, dinosaur storage and audit systems. Server-side access controls and community policies matter as well as local application settings. Ordinary group-map visibility does not mean that the host operator has no administrative access to server data.

Use **Forget remembered account** to remove the local remembered link and revoke it on the host when connected. Disconnect voice before changing audio hardware. For account-data questions, contact staff privately through a ticket.

## Updates and saved settings

When an update is offered, use the application's update prompt or an official GitHub release. The in-app updater downloads and validates the installer before handing it to the installer process.

The normal update flow preserves local preferences and the remembered device link for the same Windows user. Points, stored dinosaurs and market records are held on the server, not inside the installation folder. The application reopens with its microphone off after an in-app update.

A server outage can prevent account synchronization and in-app updates even if GitHub downloads are available. A successful installer download does not mean that the game or voice server is currently online.

Before uninstalling on a shared computer, disconnect and use **Forget remembered account** if you do not want the local link retained. Removing the desktop application does not delete a server-side dinosaur inventory or account balance.

## Troubleshooting

### The account appears offline

Check that the RynxRex services are available and that you have a network connection. A remembered account can remain stored while the host is offline. Do not repeatedly re-verify solely because the host is restarting.

### I am asked to verify again

Check whether you changed Windows account/computer, removed the saved link or had the device session revoked. If the problem occurs after a normal update on the same Windows account, report the previous/current versions and exact message through a ticket. Keep the verification code out of screenshots.

### Voice connects but nobody can hear me

Check the selected microphone, push-to-talk binding or voice-activation threshold, Mute and Deafen. Confirm you have a living character and fresh position on RynxRex. Proximity voice is limited to eligible nearby players; it is not a global server broadcast.

### The overlay is missing

Make The Isle the foreground application. Check the relevant overlay option and shortcut, account connection, living-character information and Map Tracker access. A map overlay also requires active tracking. Try a compatible game display mode if the game or another overlay prevents the window from appearing.

### Store or Load does not complete

Check growth, species/sex requirements, health, movement during warmup and storage capacity. Wait for the final server response. For a locked record, provide the dinosaur ID, attempted action and time to staff. Do not keep resubmitting a pending transaction.

### Colors differ from the preview

The preview is a reference render. Species, growth, skin pattern and lighting affect appearance. If Done reports success but the live dinosaur does not change, report the dinosaur species, time and relevant screenshots. The preview alone is not proof that a server-side repaint succeeded.

### Windows or antivirus software blocks the installer

Use the security section above. Verify the official source and hash, scan the exact file and retain the detection details. Do not disable protection or assume every detection is a false positive.

## Support and tickets

[Join the RynxRex Discord](https://discord.gg/H5ugndhwAW), read the rules and open **#open-a-ticket**.

Available categories include general support, player reports, game ban appeals, Store/Load/market problems, technical bugs and account/Points/boost questions.

Prepare:

- Your in-game name and Steam64 ID.
- Your Companion version.
- The approximate date/time and your time zone.
- What you expected and what actually happened.
- Any dinosaur or transaction ID relevant to the case.
- The exact error and useful screenshots or evidence.

Tickets are private to the author, authorized staff and any explicitly invited witnesses. Staff can add or remove a witness with `/ticket_add` and `/ticket_remove`. Closed tickets are archived for staff review under the community's ticket workflow.

Do not include passwords, Steam Guard codes, private verification codes, device credentials or Discord bot tokens in a ticket. Redact those from screenshots before posting.

## Release 3.23 notes

- 90 individually authored complete skin designs across six rarity tiers.
- Distinct Mythic base combinations and coordinated animated accents.
- New palette values kept within SDR ranges to reduce washed-out highlights.
- Compatibility retained for previous applied/stored color data and legacy animation identities.
- Private in-game welcome directing joining players to Discord and the server rules.
- Packaged installation/uninstallation and update integrity checks completed during release preparation.

The host-side Discord bot and its tickets/information channels are maintained separately from this installer. Their deployment does not require distributing bot credentials or server-management files to players.

## Important limits

- A README, a file hash and a clean antivirus result are evidence with specific scopes, not an absolute safety guarantee.
- No independent security audit or VirusTotal certification is claimed here.
- No live 400-player performance certification is claimed.
- Game updates, server capabilities and reference-map changes can affect features.
- The RGB-wave client-mod experiment is not part of this release.
- The proposed rewards for exactly two active Discord boosts are not advertised as active: the documented bot API does not provide a reliable exact active boost count per member.
- Prices, access rules and enabled server features can change. Check current in-app information and official announcements.

**RynxRex • Survive. Evolve. Connect.**
