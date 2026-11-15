# Umbrella Family

### Thoughtful controls for family movie nights

An independent Kodi add-on with optional scene skipping, subtitle-based word silencing, and a Parent Audit mode to help adults review filters before watching together.

[Install & download](https://ccherbst.github.io/umbrella-family-repo/) · [Repository installer](https://ccherbst.github.io/umbrella-family-repo/repository.umbrellafamily-1.0.0.zip) · [Report an issue](https://github.com/CCHerbst/umbrella-family-repo/issues)

---

## Release status

| | |
| :--- | :--- |
| Current release | **Beta 12** · `6.8.01+family.12` |
| Supported Kodi version | **Kodi 21 Omega** — including 21.1 and 21.3 on Fire TV |
| Update channel | Public beta |
| Add-on name in Kodi | **Umbrella Family** |
| Installation identity | `plugin.video.umbrellafamily` — separate from original Umbrella |

**Experimental, not a child-safety guarantee.** Filter coverage, editions, timing, seeking, and subtitle accuracy vary. An adult should review each title and source before children watch. Recent availability, timing, subtitle-download and audit features still need FireStick validation; credentialed OpenSubtitles downloading has not yet been live-tested. Do not rely on this beta for unattended viewing.

### New in beta 12

- **Playback controls:** open the playback OSD (usually Select/OK on Fire TV) during filtered playback for play/pause, back 10 seconds, forward 30 seconds, next filter interval, filter review/timing, Kodi controls, hide and stop.
- **Filters stay active:** hiding the panel or opening details does not disable filtering. Category and timing changes still require stopping and restarting through review. Parent Audit remains a separate, explicitly unfiltered mode.
- **Parent Audit startup correction:** dialog cleanup now finishes before playback resolution, and the audit overlay has its own Kodi callback thread. These changes address an identified startup race; the reported Glass Onion/CleanStream hang still needs confirmation on FireStick Kodi 21.3.
- **Validation:** 275 automated tests pass. Remote behavior and layout still need device testing; this is not a safety certification.

### Also included from beta 11

- **Combined source-list availability:** CleanStream for movies; VideoSkip for movies and exact TV episodes. Cached background checks distinguish filters found, none found in search, failures and incomplete searches. Availability is not a stream/edition match.
- **Inspect before playback:** on a source, press the remote's Menu button and choose **Family filter availability / VideoSkip details** to read filter editions and notes without downloading/applying a filter.
- **Manual landmark timing:** Parent Audit can show a provider reference, seek in one-second steps and mark a paused matching landmark. Saving requires confirmation and applies only to that exact stream/filter; subtitle offsets and global defaults stay unchanged.
- **Optional subtitle discovery:** find an SRT before playback through OpenSubtitles, then silence matching caption intervals. Requires your own Family API key and OpenSubtitles account. File import remains the default; downloads require explicit approval and may count against provider quotas.

Source-list checks send the movie/show title to VideoSkip; they never send stream URLs. Disable **Show CleanStream / VideoSkip availability above sources** to stop these browsing-time checks. Subtitle downloads are opt-in. No audible bleeps or live speech recognition are included.

## Install once. Update through Kodi.

1. In Kodi, open **Settings → System → Add-ons** and enable **Unknown sources** if needed.
2. Go to **Settings → File manager → Add source** and enter:

   ```text
   https://ccherbst.github.io/umbrella-family-repo/
   ```

   Name the source **Umbrella Family**.
3. Open **Add-ons → Install from zip file → Umbrella Family** and select **`repository.umbrellafamily-1.0.0.zip`**. This installs the update repository, not the video add-on itself.
4. Choose **Install from repository → Umbrella Family Repository (Beta) → Video add-ons → Umbrella Family → Install**.
5. Open Umbrella Family's add-on information page and leave **Auto-update** enabled. Kodi's global add-on update policy must also allow automatic updates.

Future **published** versions arrive through Kodi. Editing the development code alone does not release an update. Kodi checks periodically; use **Check for updates** in the add-on browser when you want to check sooner.

### Fire TV: if selecting a network ZIP closes Kodi

Use Kodi's File manager to copy the repository ZIP to a local folder first. If needed, add `special://home/` as a second File manager source named **Kodi Local**. Select the ZIP in the network source, open its context menu with the remote's **☰** button, and choose **Copy** with Kodi Local open in the other pane. Then use **Install from zip file → Kodi Local**. Restart Kodi after installation.

### Moving from the earlier manual betas

The earlier beta ZIPs replaced the original Umbrella add-on. This release has its own identity and does **not** automatically overwrite or copy the old profile.

1. In the old beta, open **Tools → Export settings** and save the backup locally. Include only the account information you intend to transfer when prompted.
2. Install this repository and Umbrella Family as described above.
3. In the new Umbrella Family, choose **Tools → Import settings** and select that backup. Review the confirmation, then restart Kodi.
4. Disable the old beta to avoid duplicate background account activity. Recreate any skin shortcuts that still point to the old add-on.
5. Recheck Family Filters, provider selection, audio handling, and timing on an adult-only test playback.

Preference/account export is selective, not a full profile backup. Existing filter files, caches, saved per-source timing, and library shortcuts are not migrated automatically. You can reauthorize accounts if your older version does not offer export. Backups that include accounts contain sensitive information: keep them private and never attach them to an issue.

## What is included?

| Feature | Purpose |
| :--- | :--- |
| Scene filtering | Skip or mute marked intervals from supported EDL, VideoSkip, and MCF files. |
| Filter discovery | CleanStream movie lookup and VideoSkip browsing where matching records are available. Coverage is not guaranteed. |
| Source-list availability | Background movie/exact-episode checks and read-only VideoSkip edition/notes inspection. Never a guarantee that filters fit a particular stream. |
| Subtitle word silencing | Mute subtitle cues containing configured words or phrases. This is cue-based muting, not live speech recognition or generated bleeps. |
| Parent Audit | Watch unfiltered content with discreet explanatory banners; review current settings or all markers, and jump between marked scenes. |
| Playback controls | Open the playback OSD for transport controls, next selected interval, reviewed filter details and a return to Kodi controls. Filtering stays active when the panel is hidden. |
| Timing tools | Save adjustments for an exact stream/filter revision; manually mark a reference in Parent Audit or experimentally propose visual alignment, subject to adult approval. |

Family Filters is **off by default**. Enable it under **Settings → Playback → Family Filters (beta)** and configure it before testing. Parent Audit intentionally plays the original unfiltered video and audio; use it without children present. TV filtering requires episode-matched records; movie-only lookup does not imply episode coverage.

## Downloads & verification

- **Recommended:** [Repository installer](https://ccherbst.github.io/umbrella-family-repo/repository.umbrellafamily-1.0.0.zip) — install once for Kodi-managed updates.
- **Manual fallback:** [Kodi 21 add-on ZIP](https://ccherbst.github.io/umbrella-family-repo/omega/plugin.video.umbrellafamily/plugin.video.umbrellafamily-6.8.01+family.12.zip) — does not install the update repository.
- [SHA-256 checksums](https://ccherbst.github.io/umbrella-family-repo/SHA256SUMS)
- [Corresponding source ZIP](https://ccherbst.github.io/umbrella-family-repo/source/umbrella-family-6.8.01+family.12-source.zip) — includes source, build tooling, tests, and notices.
- [License](https://ccherbst.github.io/umbrella-family-repo/LICENSE.txt)

This is a **public distribution repository**, not an unpacked application source tree. It contains installable ZIPs, update metadata, documentation, and presentation assets. Kodi add-ons are Python-based, so application code necessarily exists inside the installable ZIP. The matching source archive is provided with the GPL license notices.

## Support & project information

When reporting an issue, include your Kodi version, device, Umbrella Family version, and a short description of what happened. Remove account tokens, streaming URLs, and personal information from logs. Please report issues to this project, not the official Kodi or original Umbrella support channels.

Umbrella Family is an independent modified distribution of [Umbrella](https://github.com/umbrellaplug/umbrellaplug.github.io). Original copyright and license notices are retained. This project is not affiliated with Kodi, Amazon, the original Umbrella maintainers, or filter providers. It does not host movies or television shows. Use only content you are authorized to access.
