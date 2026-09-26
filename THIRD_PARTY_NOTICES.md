# Third-party notices

GPT输入法 derives its native input engine from Trime and uses Rime Ice data. The custom frontend and project are distributed under GPL-3.0-or-later; retain these notices and corresponding source when redistributing.

| Component | Source / fixed version | License location |
|---|---|---|
| Trime JNI | https://github.com/osfans/trime — v3.3.12, e09ac7114fa067904ed358e82d499516cb423ff4 | LICENSE; upstream/trime-jni source headers |
| Rime Ice dictionaries, schemas, Lua, OpenCC data | https://github.com/iDvel/rime-ice — 3aea6d3694fb3d94ec663641f021f788822897ad | app/src/main/assets/RIME-ICE-LICENSE.txt; original asset headers |
| librime and plugins | Recursive revisions in upstream/submodule-commits.txt | upstream/trime-jni/librime and rime-* license files |
| OpenCC | Recursive revision in submodule manifest | upstream/trime-jni/OpenCC/LICENSE |
| glog, yaml-cpp, leveldb, marisa-trie and their dependencies | Recursive revisions in submodule manifest | upstream/trime-jni/librime/deps/* license files |
| Snappy | Recursive revision in submodule manifest | upstream/trime-jni/snappy/COPYING |
| Boost | 1.89.0, downloaded by upstream CMake using pinned SHA-256 | Boost Software License 1.0 in downloaded source |
| Rime prelude default configuration | Trime v3.3.12 bundled assets / prelude revision in manifest | Original headers preserved |
| Android desugar_jdk_libs | 2.1.5 | https://github.com/google/desugar_jdk_libs (GPLv2 with Classpath Exception and upstream notices) |
| Gradle wrapper / Android Gradle Plugin | 8.11.1 / 8.9.1 | https://github.com/gradle/gradle ; https://android.googlesource.com/platform/tools/base |
| JUnit and JSON-java (tests only) | 4.13.2 / 20240303 | https://github.com/junit-team/junit4 ; https://github.com/stleary/JSON-java |

Native binary provenance: the two SHA-256 values in versions.json identify the downloaded official Trime release APKs from https://github.com/osfans/trime/releases/tag/v3.3.12, not a locally reproduced native build. The original unmodified libraries are included alongside matching pinned source. Build tooling may download the fixed external build dependencies. Dictionary headers contain their original dataset attribution.


## 2.2.0 派生词库索引

`dictionary-catalog.db` 由随附雾凇中英文词库生成，词条许可证与各原始词库相同。生成脚本为 tools/build_dictionary_catalog.py，无新增外部语料。
