# Third-party notices

This file summarizes third-party material used by W40KRT_VR. The release archive contains the applicable full license texts. Components remain subject to their own terms and are not relicensed by the project's MIT License.

## Rogue Trader VR (RTVR)

Managed game and UI integration includes code adapted from [Rogue Trader VR](https://github.com/SolemnScribe/rogue-trader-and-pathfinder-vr), copyright © 2026 SolemnScribe, under the MIT License. The retained license is available in [`LICENSE-RTVR`](../LICENSE-RTVR).

## Khronos OpenXR SDK

The native bridge uses the Khronos OpenXR SDK loader and headers from release 1.1.63. Khronos material retains its Apache-2.0, MIT, and related notices. The optional OFXR provider vendors the generated OpenXR headers required to build its API layer, with the corresponding Apache-2.0 and MIT texts.

## JsonCpp

The statically linked OpenXR loader includes JsonCpp. Its public-domain dedication and accompanying notices are preserved in the release archive.

## NVIDIA

The downloadable release includes the signed NVIDIA DLSS runtime 310.9.1.0 and an NGX integration. These components remain subject to NVIDIA's license terms and are not covered by the W40KRT_VR MIT License.

The optional OFXR provider uses the public D3D12 interface headers from NVIDIA Optical Flow SDK 5.0.7. Their permission notice is retained with the provider source. The provider dynamically loads the Optical Flow API from the installed NVIDIA display driver and does not redistribute an Optical Flow SDK binary.

## Optional OFXR provider

The optional provider is based on **[OFXR Bridge](https://github.com/tig3rmast3r/OFXR-Bridge), created by tig3rmast3r**, and is distributed under **LGPL-3.0-or-later**. Its corresponding source and W40KRT_VR modifications are included under [`third_party/ofxr`](../third_party/ofxr), together with its license and build information.

The provider uses AMD FidelityFX SDK Optical Flow components under AMD's MIT License. FidelityFX source is a build-time input and is not included in this repository; the required upstream version is documented with the provider source.

## ESO space background

The Space-combat background uses an adaptation of **IC 2631**, credited to ESO.

- Source: <https://www.eso.org/public/images/eso1605a/>
- License: [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)
- Adaptation: square framing, darkening and colour treatment, border fade, and runtime export.

## Microsoft Visual C++ Redistributable

The downloadable installer includes the official Microsoft Visual C++ x64 Redistributable. It is verified before execution and remains subject to [Microsoft's redistribution terms](https://learn.microsoft.com/en-us/cpp/windows/redistributing-visual-cpp-files).

## Components obtained from the game

Unity, Harmony, Newtonsoft.Json, Unity Mod Manager, game assemblies, and game assets are referenced or loaded from the user's legitimate *Warhammer 40,000: Rogue Trader* installation. They are not distributed as source or relicensed by this repository. Runtime servo-skull hand visuals are loaded from the installed game and are not included here.

## Distribution policy

Only redistributable runtime dependencies are bundled. Full applicable notices are retained under [licenses](.) and inside each release archive. Proprietary SDK packages, game assemblies and game resources are not supplied. See [Distribution and licenses](../docs/DISTRIBUTION.md).
