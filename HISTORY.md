# Pathology — release history

## v4.3.46 — 2026-11-17

- toast start failures from tray / Core Host initiated starts
- wire the 1.5 track (sing-box-pathology) into the repo layout
- local 1.5 dev build via docker (no push, no client conflict)
- engine 1.5 group wrappers in profile pipeline
- surface dropped/migrated subscription nodes in the UI
- chain 2.0 — group wrappers as exits + readable path
- emit engine-1.5 syntax from control-plane mappers
- thread duplicate-tag warnings through source compile (leftover of the parse-warnings surfacing)
- local build stages the core into bin/ (it is a build input, never read by the running client) — fixes Flutter install step
- pathology protocol (engine 1.5) client+server mappers
- mesh (bb_mesh) UI section
- add parse-warning keys to all locales (en text as placeholder)
- pathology preset seed family (13 curated) + preset-only UI selection
- auto rotation = builder-synthesized group (CP emits only the parent)
- pathology auto = legend set x4 (stun/tls/quic/ssh) + first-alive rotation
- close the 1.5 migration re-audit client punch-list + pin bumps
- pathology:// with an authority is a WG share, not a deep link
- bake the 1.5 controlplane tag on the 1.5 track
- merge ref-key SSOT, dangling-hop sweep, legend virtuals in leaf pool
- cycle guard, serialized mesh sync, validation + mesh knobs
- scope the wrapper sweep to damage it caused, keep allowlist in step
- pin per-legend demux rule network to the legend branch
- shared duplicate-tag predicate, wrapper-liveness allowlist parity
- report on build/retry paths, profile-scoped dedup, bounded heal state
- 1.5 endpoint classification, wrapper-aware server sync, mapper fixes
- dual-stack listen for server inbounds on IPv6 hosts
- implement the sing-box 1.5 PlatformInterface additions
- make the extracted AppDir readable before repacking the AppImage

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.46)

## v4.3.44 — 2026-10-29

- never bake an unpublished subserver image tag

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.44)

## v4.3.42 — 2026-10-27

- Maintenance release

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.42)

## v4.3.40 — 2026-10-27

- bundle a complete sqlite3 - the mirror artifact was missing symbols
- build SQLite from a vendored amalgamation with column metadata

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.40)

## v4.3.38 — 2026-10-26

- open the database in the current isolate, not drift_flutter's

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.38)

## v4.3.37 — 2026-10-26

- seed profile streams from a one-shot read; keep app.log alive [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.37)

## v4.3.36 — 2026-10-25

- ownership-based core host, real TUN caps, profile invariants [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.36)

## v4.3.34 — 2026-10-23

- working autostart (login + boot service), visible tray icon [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.34)

## v4.3.33 — 2026-10-22

- list-only server delete, subserver-port ping, fresh-image installs, VPS setup [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.33)

## v4.3.32 — 2026-10-20

- setcap both binaries (caps don't cross exec; tun is created by the spawned PathologyCli) + pin core e6220bba (PathologyCli soname link - was NEEDED ./lib/pathology-core.so resolved against process cwd -> black window on terminal launches) [skip ci]
- Cascade egress excludes server-owned profile leaves (no self-loop) + hide profiles left with no leaves; rename Outbounds->Cascade (11 locales); wipe-confirm guard no longer fires on empty WG (sticky everPublished false positive) [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.32)

## v4.3.30 — 2026-10-15

- force /usr/bin/pathology symlink in postinst (packager's bare ln -s loses to a stale file from an old manual install -> binary can't find bundled libs) [skip ci]
- dual RUNPATH $ORIGIN/lib + /opt/pathology/lib - glibc drops $ORIGIN under AT_SECURE (deb postinst setcap for rootless TUN), so non-root deb runs failed to load bundled plugins [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.30)

## v4.3.29 — 2026-10-15

- Punnel/demux semantics made logical: punnel-owned demux sets accept user port slots and members (punnel is a priority matcher, not a port capturer); punnel-managed slots keep per-slot armor; fallback/members tiles on punnel slots are disabled with a hint; sets now show a read-only Punnel rules card (service, match kind, SNI, port) linking to the Punnel page; sets that lose all punnel content become editable again

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.29)

## v4.3.28 — 2026-10-13

- PathologyWG/WireGuard now actually reaches subscriptions: user WG credentials (keypairs, host index, morpher key) are seeded on every server-config apply and after hub sync imports, not only on the WG page publish

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.28)

## v4.3.27 — 2026-10-13

- Control-plane management/subscription connections now retry transient TLS kills (probabilistic DPI/NAT cuts to bare-IP endpoints) instead of surfacing raw Dio errors; compact transport error strings
- Enabling a server-local user as a VPN profile no longer fails with profileUpsertFailed and no longer leaves duplicate profiles: the subscription compiler fetch retries transients, and a failed compile rolls the fresh profile row back
- nip.io/sslip.io host aliases: a server record can move to an SNI-carrying hostname (e.g. 104-252-111-184.nip.io) without breaking stored subscription URLs

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.27)

## v4.3.26 — 2026-10-13

- QS tile and shortcut open the app when no profile is enabled instead of connecting 'No VPN'; a stale cached start target no longer connects direct mode with zero profiles
- Home connect button always disconnects a live VPN; the guide quick-start opens only when nothing is connectable
- Android: core start failures surface via notification instead of leaving a zombie VPN service
- Releases now bake the exact control-plane image (published by the subserver repo's own CI) instead of a mutable tag

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.26)

## v4.3.25 — 2026-10-12

- Repository tile points to the public releases repo; acknowledgments reordered (sing-box, Hiddify, Neural networks block, Cursor, ZCode, rest)

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.25)

## v4.3.24 — 2026-10-12

- dual-scope theming - separate saturation/tint/brightness for page background vs content blocks, reset moved to app bar icon, scaffold follows styled surface
- guide-style link rendering (accent, bold, no underline) + clickable external links
- direct mode keeps local tun capture (DNS/filtering is its purpose); privilege guidance in MissingPrivilegeMsg [skip ci]

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.24)

## v4.3.23 — 2026-10-11

- retire home-background customization; global surface theming takes over (saturation / tint intensity / brightness sliders, stronger preset bases)
- license OTA (signed-by-hash remote revisions, 12h check, re-accept on new version, legacy accepts preserved) + Version history page fed by public HISTORY.md
- open-file dialogs via file_selector/xdg-portal (file_picker's modal GTK dialog stalls the embedder main loop), file_picker fallback

[GitHub](https://github.com/ne-tort/Pathology-Client/releases/tag/v4.3.23)
