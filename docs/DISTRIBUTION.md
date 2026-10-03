# Distribution, licenses and credits

This repository provides ready-to-install W40KRT_VR releases and player documentation. The original mod's buildable source, development project, internal tools and development history are not published here. Installation scripts and configuration files needed to run the supplied package remain included. Third-party corresponding source required by its license remains available.

## Original work

The original W40KRT_VR work in **0.9.79, 0.9.80 and 0.9.81 beta** retains its existing [MIT License](../LICENSE), copyright 2026 Beren5556. Binary distribution does not revoke that grant or impose new restrictions on copies already released under MIT. MIT does not require delivery of the original source. Preserve its copyright and permission notice when redistributing covered material. The software is supplied as is, without warranty, on the terms stated in that license.

This notice is specific to the supplied versions. It does not grant a blanket MIT license over every future component: each release must identify the terms covering its original components. Third-party components always retain their own licenses.

## Third-party work

- **SolemnScribe — Rogue Trader VR (RTVR):** adapted game, camera, renderer and interface integration under MIT. The original copyright and permission notice remain in [LICENSE-RTVR](../LICENSE-RTVR). [Upstream project](https://github.com/SolemnScribe/rogue-trader-and-pathfinder-vr).
- **tig3rmast3r and OFXR Bridge contributors:** the optional modified OFXR provider remains under LGPL-3.0-or-later. The [versioned corresponding source archives](../third_party/ofxr) contain modifications, build files, LGPL and incorporated GPL texts, and dependency notices. The 0.9.80 and 0.9.81 source archives are also included in their installable ZIPs. These modifications are not withheld as private mod code.
- **Khronos and JsonCpp contributors:** OpenXR loader, headers and associated notices retain their applicable licenses. The core loader and the OFXR header subset use the revisions identified in their respective notices.
- **NVIDIA:** the DLSS runtime, NGX integration and permitted Optical Flow interface headers retain their own terms. NVIDIA components are not made MIT-licensed by inclusion. The provider loads Optical Flow from the installed display driver; the full proprietary SDK is not redistributed.
- **AMD:** linked FidelityFX Optical Flow components retain AMD's MIT notice. The exact upstream source revision is identified in the OFXR source's build documentation.
- **Microsoft:** the official Visual C++ Redistributable remains subject to Microsoft's terms. Redistribution of that runtime does not grant rights over other Microsoft software.
- **ESO:** the adapted IC 2631 space background retains its credit and [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) terms. See [the original image](https://www.eso.org/public/images/eso1605a/) and [the adaptation notice](../THIRD_PARTY_NOTICES.md).

Full notices accompany the downloadable package and are also collected under [licenses](../licenses). See [THIRD_PARTY_NOTICES.md](../THIRD_PARTY_NOTICES.md) for component details.

## OFXR source and replacement

The OFXR provider is a separately loaded library. The source archive preserves the layout and shared MIT interface header needed to build a compatible replacement. Start with the archive's `BUILDING.md`, then follow `optional/ofxr/provider/docs/BUILDING.md` for the pinned SDK dependencies and Release build.

Users may modify and rebuild the LGPL-covered library and replace its installed provider DLL with an interface-compatible build. Preserve a recoverable copy, close the game before replacement, and keep the provider's required dependencies together. The supplied installer verifies the official package; use a manual library replacement for your modified build. The applicable LGPL rights, including reverse engineering to debug modifications to the library, are preserved. This does not provide a warranty or support commitment for modified builds.

## Game and external software

The game, game assemblies, models, textures, audio, trademarks and other game assets are not covered by this project's license and are not redistributed. Unity, Harmony, Newtonsoft.Json and the game's mod loader are obtained from the user's legitimate game installation. Servo-skull visuals are loaded from that installation.

Headset connection software, display drivers and purchased products such as Virtual Desktop must be obtained separately under their own terms. Only dependencies whose redistribution is permitted are bundled.

W40KRT_VR is an independent, non-commercial fan project. It is not affiliated with, sponsored by or endorsed by Owlcat Games, Games Workshop, NVIDIA, Meta, Virtual Desktop or dependency authors. All trademarks belong to their owners.
