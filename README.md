# Warhammer 40K: Rogue Trader VR

**W40KRT_VR — The depth of Rogue Trader, on your tabletop.**

> **Public PC beta · OpenXR · English and Spanish**

W40KRT_VR turns *Warhammer 40,000: Rogue Trader* into a virtual-reality experience built around a three-dimensional tabletop. Move around the scene, bring it closer, and manipulate it with Touch controllers as if the adventure were laid out in front of you.

The approach is reminiscent of **Demeo**, while preserving the original game's campaign, rules, combat, and decisions. Watch the action from above, use closer character views, or enter first person.

## Download

**[Download 0.9.81 beta](https://github.com/Beren5556/W40KRT_VR-Downloads/releases/download/v0.9.81-beta/W40KRT_VR-0.9.81-beta.zip)** · [Release notes](docs/RELEASE_0.9.81.md) · [All releases](https://github.com/Beren5556/W40KRT_VR-Downloads/releases)

Download the named **W40KRT_VR-0.9.81-beta.zip** release asset and extract it completely. GitHub's automatically generated **Source code** archives contain repository documentation and third-party material; they are not the installable mod.

This is the official binary-distribution repository for W40KRT_VR. It provides ready-to-install packages, player documentation, credits, license notices, and required third-party source. The original mod's buildable source and development project are not distributed here. See [Distribution and licenses](docs/DISTRIBUTION.md).

## Main features

- **Manipulable VR tabletop:** move, rotate, tilt, and scale the scene with controller gestures.
- **Full headset tracking:** inspect the world from different physical positions and angles.
- **Multiple perspectives:** switch between tabletop, character framing, and first-person views.
- **Touch controls:** select characters, issue orders, and use VR action and participant wheels.
- **Spatial interface:** use dialogue, character sheets, weapons, status information, inventory, and management screens inside the headset.
- **Game-context coverage:** On-foot exploration, Ground combat, Space combat, Star map, Galactic map, Management screens, and Dialogues and cinematics.
- **Configurable image quality:** saved profiles, adjustable resolution, TAA, and per-eye DLSS/DLAA for compatible NVIDIA GPUs.
- **Experimental OFXR:** optional frame generation for the VR output.
- **Dedicated VR launcher:** select the headset, connection, runtime, render mode, DLSS quality, and optional OFXR before starting the game.
- **Comfort options:** panel size and distance, camera movement, tabletop controls, and independent layouts for different screens.
- **Direct interface layout controls:** adjust the HUD, management screens, maps, control hints, and F1 menu from the main VR settings.
- **English and Spanish help:** contextual reminders and control guidance adapt to the current game context.
- **VR-oriented exploration interactions** and optional combat visibility settings intended to reduce rendering load.

The **Star map** is the warp-route and travel interface. The **Galactic map** shows planets within a system. Orders, abilities, movement rules, and game data remain part of the original game.

## What's new in 0.9.81

- More flexible positioning for dialogue, management, large tutorial, and tip panels, with corrected clipping and revised initial layouts.
- Shared horizontal, vertical, and distance controls for the mod menu and its illustrated tutorial.
- Unified management-screen settings while retaining the game's native navigation and window behaviour.
- Improved camera follow near scenery and 40% faster default stick rotation and tilt.
- Selectable DLSS and DLAA models: **Automatic, J, K, L, and M**, subject to GPU and runtime support.
- A main-menu switch for monitor output, useful when comparing performance or keeping the VR image off the desktop.
- Revised clean-install defaults for interface placement, camera movement, diagnostics, OFXR, and monitor output.
- Safer upgrades: the installer creates and verifies a recoverable backup before applying the revised settings and saved layouts.

## Compatibility

| Component | Beta support |
| --- | --- |
| Game | Steam edition of *Warhammer 40,000: Rogue Trader*, using the build stated in the release |
| System | 64-bit Windows 10 or 11 |
| Graphics API | DirectX 11 |
| VR standard | OpenXR |
| Physically validated headsets | Meta Quest 3, PICO 4/4 Ultra, and Pimax Dream Air/Dream Air SE SLAM |
| Virtual Desktop | Meta Quest and PICO 4/4 Ultra through VDXR |
| Meta connection | Meta Quest Link or Air Link |
| Pimax | Dream Air and Dream Air SE SLAM through Pimax Play native OpenXR |
| Mod languages | English and Spanish |

W40KRT_VR uses OpenXR directly and does not require SteamVR. PICO Connect, the legacy PimaxXR runtime, eye tracking, Quad Views, Lighthouse controllers, other storefronts, and unlisted headset combinations are outside this beta.

The mod's own interface is available in English and Spanish. Native game text and data retain the language selected in *Rogue Trader*.

## Install

1. Download the beta ZIP from [Releases](https://github.com/Beren5556/W40KRT_VR-Downloads/releases).
2. Extract the entire archive into a new folder outside the game directory.
3. Close *Rogue Trader* completely.
4. Run the single shared **INSTALL.cmd**. Do not look for a headset-specific installer: headset, connection, and runtime selection happens later in the launcher. The game uses its built-in mod loader; another mod manager is not required.
5. If the installer cannot find the game, select the folder containing `WH40KRT.exe`.
6. Connect the headset and controllers through Virtual Desktop, Meta Quest Link/Air Link, or Pimax Play as appropriate.
7. Run **LAUNCH-VR.cmd**, select the headset and connection, and press **Launch game**.

The package includes installation and removal tools. You do not need to compile anything, install RTVR separately, or add an external mod manager.

To update from an earlier version, run the installer from the new package while the game is closed. Version 0.9.81 introduces revised layout defaults, so the installer explains which mod settings and saved layouts will be reset and asks before continuing. It then creates and verifies a recoverable backup and displays its location. If the backup cannot be verified, the reset is cancelled. The selected OpenXR runtime, user-selected DLSS DLL, `Params.xml`, saves, and unrelated mods are preserved. Reinstalling 0.9.81 preserves the current mod settings. To remove this beta, use **UNINSTALL.cmd** from the matching package.

The installer also creates a **Rogue Trader VR** shortcut using the icon from the locally installed game. Starting the game normally through Steam or `WH40KRT.exe` remains flat; use the launcher or its shortcut for VR.

## VR launcher and OpenXR runtime

The English launcher supports these paths:

- **Meta Quest:** Virtual Desktop/VDXR or Meta Quest Link/Air Link.
- **PICO 4 and PICO 4 Ultra:** Virtual Desktop/VDXR only.
- **Pimax Dream Air and Dream Air SE SLAM:** Pimax Play native OpenXR.

The launcher detects or accepts the runtime file, starts DirectX 11, and applies the selected runtime only to the game process. It does not change the default OpenXR runtime in Windows or modify NVIDIA profiles. It reads the saved rendering mode, DLSS scale, and OFXR preference; changes are committed when the launch is requested and rolled back if the process cannot be started.

For the Steam edition, open Steam normally and sign in before launching VR. W40KRT_VR checks the Steam connection before saving preferences or starting the game, then opens `WH40KRT.exe` directly with the VR and DirectX 11 arguments and closes the launcher. It does not start the Steam client. If Steam is closed or unavailable, the launcher asks you to open it instead of allowing the game to start without its mods. Do not run the launcher as administrator.

## Experimental OFXR

OFXR is an optional frame-generation mode for the VR output. It can improve perceived smoothness, but results depend on the PC, scene, and configuration, and it may introduce visual artifacts or latency.

To try it, select **Experimental OFXR** in the launcher before starting VR, or enable it from the main VR settings and restart the game. If **Selective engine cadence** is active, the launcher offers an explicit choice because the two modes are incompatible.

Disable the option and restart again to return to normal rendering. OFXR works over the supported runtime paths, is off by default, and does not replace DLSS/DLAA. The in-game OFXR status reports whether synthesis is actually active; selecting the launcher option is only a request.

## Performance guidance

An **NVIDIA GeForce RTX 4080, 5080, or 4090** is recommended for the intended high-quality configuration. This is guidance rather than a minimum requirement or a guarantee of constant performance in every scene.

On less powerful systems:

1. Start with the mod's **Performance** profile.
2. Reduce **Draw distance** under Advanced settings when more headroom is needed.
3. Try either OFXR or the interpolation provided by Virtual Desktop or Meta Quest Link.
4. Select 90 or 100 Hz only when that refresh rate is available for the headset and connection method.

Compare settings in the same scene. Test interpolation methods separately before combining them. Interpolation can improve perceived smoothness, but it does not increase the real rate at which the game calculates its simulation.

## Touch control summary

Controls adapt to the current game context.

| Action | Control |
| --- | --- |
| Point and select | Aim with the right skull and press the right trigger or **A** |
| Frame a character, enemy, or ship | Double-click the target |
| Enter first person | Fully hold the right trigger for 2 seconds over a character or ship |
| Move and enter first person | Hold over a valid destination for 2 seconds in exploration or 3 seconds in Ground combat |
| Leave first person | Press **B**, or bring both gripped hands together |
| Select a group | Hold the right trigger and drag a selection rectangle |
| Move the party during exploration | Right stick, relative to the selected character's heading |
| Move the tabletop | Hold either grip and move that hand |
| Rotate and scale the tabletop | Hold both grips; rotate the hands or change the distance between them |
| Rotate or tilt with a stick | Left stick |
| Open the left wheel | Left grip + left trigger |
| Open the right wheel | Right grip + right trigger |
| Switch actions and participants | Click the left stick while the left wheel is open |
| Read cards and information | Point at a left-wheel item and hold the right grip; use the right stick to scroll |
| End the turn | Hold the left stick, **A**, or right trigger for 1 second over the end-turn skull |
| Tactical information | Hold **Y** during the player's Ground-combat turn |
| Interact and highlight in exploration | **A** interacts; hold **Y** to highlight available objects |
| Cancel, go back, or close | **B**; the left trigger retains the native secondary click |
| Pause or resume | **X** |
| Toggle contextual reminders | Short right-stick click |
| Open or close VR settings | Hold both triggers and both grips for 1 second, or press **F1** |

On the Star and Galactic maps, use the right stick to pan and the left stick up/down to zoom. The warp-route Star map uses the native right options bar; the system/planet map retains its right wheel. Native windows and dialogue use the right-hand pointer with the right trigger or **A**; the right stick scrolls and **B** goes back when allowed by the game.

The mod includes contextual help and an illustrated in-game control guide.

## Beta status

W40KRT_VR remains in public beta. Version 0.9.81 expands interface placement, camera control, DLSS/DLAA selection, monitor-output control, and experimental OFXR compatibility. The listed Meta, PICO, and Pimax paths have been physically validated. Performance can still vary between PCs and during combat or complex scenes, and this release does not claim a measured FPS improvement.

This is a personal project without formal technical support. Experiences and questions may be discussed in community forums, without a commitment by the author to respond, investigate, or provide fixes.

Release notes will focus on player-visible features, improvements, and relevant known limitations.

## Possible future improvements

These items are being considered and are not promised for a particular release:

- Hand Tracking as an alternative or complement to Touch controllers.
- Interaction with hyperlinks that open additional information in game windows.
- Further OFXR development and tuning.
- Broader compatibility with additional headsets and connection methods.
- Additional combat performance and stability work.
- Additional camera, interface, and control options.

## Credits

This project incorporates code adapted from **Rogue Trader VR (RTVR), by SolemnScribe**, released under the MIT License. Its work integrating *Rogue Trader* with the cameras, renderer, and interface provided an important foundation for this adaptation.

Without that initial work, substantially more time would have been required to investigate camera integration, move the menus into three-dimensional space, preserve interaction, and solve compatibility and scene-transition problems. Many thanks to SolemnScribe for sharing this work and source code with the community.

Building on that foundation, W40KRT_VR develops its own tabletop approach inspired by **Demeo**: a direct OpenXR bridge for VDXR and Meta Quest Link, full headset tracking, Touch controls and gestures, multiple camera perspectives, and extensive interface, comfort, and rendering work.

The experimental frame-generation mode is based on **[OFXR Bridge](https://github.com/tig3rmast3r/OFXR-Bridge), created by tig3rmast3r** and released under LGPL-3.0-or-later. Many thanks to tig3rmast3r for creating OFXR Bridge and sharing its source with the VR community. W40KRT_VR adapts and integrates that technology as an optional, game-specific component that is disabled by default.

- [RTVR on Nexus Mods](https://www.nexusmods.com/warhammer40kroguetrader/mods/518)
- [SolemnScribe's source code](https://github.com/SolemnScribe/rogue-trader-and-pathfinder-vr)
- [OFXR Bridge by tig3rmast3r](https://github.com/tig3rmast3r/OFXR-Bridge)

## License and intellectual property

The original W40KRT_VR work included in version 0.9.81 retains its existing [MIT License](LICENSE), copyright 2026 Beren5556. Distributing binaries without the original buildable source does not revoke that grant. Adapted RTVR code retains SolemnScribe's copyright and MIT terms in [LICENSE-RTVR](LICENSE-RTVR). The optional OFXR provider is distributed under LGPL-3.0-or-later; its corresponding source, modifications, and build instructions are supplied [here](third_party/ofxr) and inside the release ZIP. Component-specific terms govern each download; this repository does not grant MIT rights over every bundled dependency.

Third-party components and assets retain their own terms. The relevant notices are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and in the license files supplied with the release package.

The W40KRT_VR license does not cover *Warhammer 40,000: Rogue Trader*, its assets, models, textures, music, trademarks, or other game content. Runtime visuals such as the servo-skull hands are loaded from the user's legitimate game installation and are not redistributed by this project.

**W40KRT_VR is an unofficial, non-commercial fan project.** It is not affiliated with, sponsored by, or endorsed by Owlcat Games, Games Workshop, NVIDIA, Meta, Virtual Desktop, or the authors of its dependencies. All trademarks belong to their respective owners.
