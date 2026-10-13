# Pathology — release history

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
