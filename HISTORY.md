# Pathology — release history

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
