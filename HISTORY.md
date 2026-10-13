# Pathology — release history

## v4.3.26 — 2026-10-13

- QS tile/shortcut open the app when nothing is connectable (stale cached start target connected 'No VPN' with zero profiles); connect button always disconnects a live session; core pin a17a205f [skip ci]
- Wire Kotlin props are snake_case (core_state/message_type); ci(cp): subserver-controlplane triggers on pathology+gitlink, publishes :sha-<pin>; releases bake controlplane_image=ghcr...:sha-<pin> via CP_IMAGE [skip ci]

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
