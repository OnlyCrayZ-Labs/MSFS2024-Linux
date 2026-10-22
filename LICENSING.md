# Licensing, attribution and distribution boundaries

**Source-only candidates. The Proton integration manifest excludes the full Proton/SDK source tree and its ancestry.**
This is a component inventory, not a blanket license or a legal clearance.

| Component | Inspected license | Required treatment |
| --- | --- | --- |
| xodus-gaming/xodus | Root LICENSE: GPL version 3 | Keep full license and copyright notices; document modifications. For conveyed binaries provide compliant Corresponding Source and any applicable installation information. Do not assume an unspecified later-version grant. |
| xodus-gaming/Proton | LICENSE is a license index; LICENSE.proton is BSD-3-Clause-style | Preserve Valve's actual notice, conditions and disclaimer. Follow each bundled component's license separately. |
| xodus-gaming/wine | LICENSE/COPYING.LIB: LGPL 2.1; Wine headers grant 2.1-or-later | Preserve notices, mark modifications, provide required source/build/relink information for binary distribution. Third-party directories have their own terms. |
| xodus-gaming/xgameruntime, selected legacy-C line | Root LGPL 2.1; source headers include or-later grants | Preserve those notices and grants. Review new files' provenance and upstream attributions. |
| Microsoft libHttpClient (on a different local xgameruntime ref) | Public upstream MIT plus NOTICE/ThirdPartyNotices | MIT permits reuse subject to its notice conditions. A local historical import has LGPL-style headers; establish original notices before conveying that ref. This import is not an ancestor of the tested legacy-C HEAD. |
| XAL / eappx Git dependencies | MIT license files checked at the exact locked revisions | Preserve exact upstream LICENSE/NOTICE at the locked revisions. |
| ntfs Git dependency | MIT OR Apache-2.0 at locked revision; both license texts checked | Preserve license/notices and modification notices as applicable. |
| Proton submodules, Rust crates, SDK/toolchain components | Mixed licenses | Build an exact pinned inventory before distributing binaries; the parent license does not cover them all. |
| Original hub documentation | GPL-3.0-only; full text in LICENSE | Copyright (C) 2026 OnlyCrayZ-Labs contributors. Component code, third-party images and trademarks retain their own terms. |

## Scope

This release scope is experimental source code and documentation only.
Do not publish the private working-runtime backup, executable game files,
Microsoft runtime DLLs copied from the installation, packages, game video/audio,
keychain exports, tokens, signatures or license/key material. User ownership of
the game is not redistribution permission. Public GDK documentation is not
permission to redistribute all GDK SDK headers, import libraries or binaries.
Publicly licensed Microsoft open-source code is distinct from proprietary SDK
code and must retain its own notices.

Before any binary release, complete the dependency/license inventory, reproduce
all build flags, prepare exact corresponding source and scripts, and check
codec/redistributable/trademark obligations. Source-only publication does not
remove the requirement to verify the source itself is publishable.

## Attribution and provenance

Credit xodus-gaming, the Wine project, Valve/Proton and dependency authors.
Retain existing AUTHORS, COPYRIGHT, LICENSE*, COPYING* and NOTICE* files; do not
replace them with an OnlyCrayZ-Labs blanket license. Modified-file notices and
a public change/provenance record must identify the upstream base and changes.
A third-party contribution cannot be relicensed by declaring it newly authored.
Check the exact files and revisions, not only GitHub's license badge.

The legal/provenance gate includes local interface/IDL/error definitions,
original taskqueue/async/save implementations, imported third-party material,
and protocol/security-related upstream code. No leaked source, NDA SDK material
or proprietary code has been confirmed by this review; pattern scanning cannot
prove its absence. Resolve unknown provenance before publishing affected files.

## Primary sources consulted

- https://github.com/xodus-gaming/xodus/blob/main/LICENSE
- https://github.com/xodus-gaming/wine/blob/bleeding-edge/LICENSE
- https://github.com/xodus-gaming/wine/blob/bleeding-edge/COPYING.LIB
- https://github.com/xodus-gaming/xgameruntime/blob/main/LICENSE
- https://raw.githubusercontent.com/ValveSoftware/Proton/proton_10.0/LICENSE.proton
- https://github.com/microsoft/libHttpClient/blob/main/LICENSE.md
- https://github.com/microsoft/libHttpClient/blob/main/NOTICE.txt
- https://github.com/microsoft/libHttpClient/blob/main/ThirdPartyNotices.txt

Local pinned license files control the inventory; online default branches can
change. This inventory records the inspected state rather than certifying every
historical file or dependency as legally cleared.

## Pinned dependency review

- XAL `6aa2420f8f0d5e6f7460ff13f399037583a942f4`: MIT, Team OpenXbox.
- eappx `e39222821f8004c663f61a917304e8f5f679b224`: MIT, tuxuser.
- ntfs `5edc794c3ec73a2722dad24abefd05f270d3e066`: MIT OR Apache-2.0;
  preserve the chosen applicable license and notices.

Their pinned LICENSE files were inspected locally; these dependencies are fetched
from their own public repositories and are not vendored by the hub. Binary
distribution remains a separate review. Proton's upstream lsteamclient contains
Steamworks SDK source under separate Valve SDK terms. No redistribution
permission for that source is assumed from its presence in a public repository.
The full Proton source candidate is withheld until that issue is resolved.

## Selected integration publication

The selected OnlyCrayZ-Labs/xodus-proton candidate is a new root containing
integration docs, the preserved Valve top-level license and a Wine gitlink.
It does not convey upstream Proton/Steamworks SDK source or its Git ancestry.
The full-history alternative remains withheld; the selected manifest's original
docs use BSD-3-Clause-style terms and do not relicense linked components.
