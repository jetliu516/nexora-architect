# Nexora Architect

Residential design workspace for the web and iPhone/iPad.

**[Open the live application](https://nexora-architect-studio-1103.jetliu518.chatgpt.site/)**

## Public source snapshot — v34

The complete source is published in [Nexora-Architect-v34-source.zip](Nexora-Architect-v34-source.zip). Download the ZIP using its **Download raw file** button. It contains 311 tracked files with their original directory structure: the web application, iOS Xcode project, tests, build tools, and development/validation documentation.

Source revision: `cfb75b33876bae5fe938a87a3c55eefeb475a4f9`. This repository currently distributes the source as an archive; the individual source files and previous development history are not expanded in the GitHub file tree.

## Run locally

```sh
unzip Nexora-Architect-v34-source.zip -d source
cd source
python3 -m http.server 8772 --directory dist
```

Open http://127.0.0.1:8772. The bundled browser editor can run without a frontend build step. AI services require separate server-side configuration and authentication. Project data is stored in the current browser; JSON export provides portable project backups.

## Test and build

From the extracted source directory:

```sh
node --test tests/*.test.cjs
```

The v34 release passed 454 automated tests. For iOS, open `ios/NexoraRoomStudio.xcodeproj`, select the `NexoraRoomStudio` scheme, and configure your signing team before running on a device. The iOS Simulator build passed; device installation and TestFlight distribution were not verified for this release.

## Contents

- `dist/`: 2D/3D editor, 100 editable residential templates, MEP tools, drawings, exports, and beam-analysis UI.
- `ios/`: native iPhone/iPad project and bundled web assets.
- `worker/`: server-side AI and research handlers.
- `tests/`: automated regression checks.
- `tools/`: build and evaluation utilities.
- `docs/`: feature matrix, implementation records, and validation limits.

Read `docs/Beam-Analysis-2026-11-09.md` and the Chief Architect feature matrix in the extracted archive for the current scope. This remains a developing design tool; full Chief Architect parity and automatic permit/code approval have not been achieved.

中文：完整源码已公开在上方 ZIP 文件中，包含网页、iOS 工程、测试及文档。下载后解压即可按上述命令运行。
