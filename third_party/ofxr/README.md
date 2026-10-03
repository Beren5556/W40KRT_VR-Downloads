# OFXR corresponding source

| Mod release | Corresponding OFXR source | Build instructions inside archive |
| --- | --- | --- |
| 0.9.81 | [Source archive](W40KRT_VR-0.9.81-ofxr-source.zip) | `ofxr-source/BUILDING.md` |
| 0.9.80 | [Source archive](W40KRT_VR-0.9.80-ofxr-source.zip) | `ofxr-provider/docs/BUILDING.md` |
| 0.9.79 | [Source archive](W40KRT_VR-0.9.79-ofxr-source.zip) | `src/optional/ofxr-provider/docs/BUILDING.md` |

The 0.9.80 and 0.9.81 archives are identical to `corresponding-source/ofxr-provider.zip` inside their respective installable packages. The 0.9.79 archive preserves the provider source from its published release tag. Use the source matching the downloaded mod version.

Based on [OFXR Bridge](https://github.com/tig3rmast3r/OFXR-Bridge), created by **tig3rmast3r**, under **LGPL-3.0-or-later**. The archive includes the modified provider, LGPL and GPL texts, dependency notices, essential build files and build instructions. Keep its directory layout intact. The shared `native/neural/Neural.h` interface header is included under its retained MIT notice because it is needed to build the provider.

For 0.9.81, extract the archive and read `ofxr-source/BUILDING.md`, followed by `ofxr-source/optional/ofxr/provider/docs/BUILDING.md`. For earlier versions, follow the paths in the table and configure `BUILD_TESTING=OFF` and `XRFG_BUILD_STANDALONE=OFF` for the provider-only build. The original mod's managed code, launcher source and native core implementation are not part of these archives.

For license scope and replacement rights, see [Distribution and licenses](../../docs/DISTRIBUTION.md).
