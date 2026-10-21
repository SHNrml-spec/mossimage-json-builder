# MOSSImage JSON Builder & Layout Studio

[![Live Demo](https://img.shields.io/badge/demo-online-brightgreen.svg)](https://shnrml-spec.github.io/mossimage-json-builder/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

🚀 **Live Web App (インストール不要で試せます)**:  
👉 **https://shnrml-spec.github.io/mossimage-json-builder/**

[English](#english) | [日本語](#japanese)

---

<a name="english"></a>
## English
An interactive, visual web tool to design and export task configuration JSON (`TASK_JSON`) for **MOSS-Image** (an open-weights text-to-image model by OpenMOSS featuring native layout control).

This tool is packaged as a lightweight, single-file HTML application (`index.html`) with **zero external dependencies** — just double-click or open it directly in any modern browser!

### 🌐 Live Demo
You can try the web application directly in your browser without installing anything:  
👉 **[Open MOSSImage JSON Builder](https://shnrml-spec.github.io/mossimage-json-builder/)**

### ✨ Key Features
- **Visual Bounding Box Canvas**: Full support for MOSS-Image coordinate specifications (`bbox_coord_space: "abs_centralized"`, `bbox_format: "yxyx"`). Drag-and-drop to create, move, and resize layout boxes.
- **Image Editing & Faint Reference Background**: Load a source image via file picker, drag & drop, or clipboard paste (`Ctrl+V`). The image renders faintly in the background with adjustable opacity (0% to 100%) so you can accurately trace and position Bounding Boxes for inpainting or editing. Includes one-click resolution auto-fit, dedicated JSON parameter support (`init_image`, `edit_mode: "inpaint"`, `denoising_strength`, `mask_feather`), and a handy "Colab fixed path" toggle switch!
- **Tag Dictionary & CSV Import/Export**: Built-in prompts/tags (quality, character, costume, composition, pose, etc.) with real-time bilingual search. Import your own CSV tags into browser local storage.
- **Japanese to English Translation**: One-click bilingual translation directly on prompt fields (via free MyMemory API with offline dictionary fallback).
- **One-Click JSON Export & Import**: Instant clipboard copy, `.json` file download, and full state restoration from existing JSON files.

### 🚀 Quick Start
1. Clone or download this repository.
2. Open `index.html` in your browser (Chrome, Edge, Firefox, Safari).
---

<a name="japanese"></a>
## 日本語
※Gemini3.8fでMOSS-ImageのjSON管理するツールを作成させたらできました。
以下、詳細

### 🌐 Webデモ（インストール不要）
ブラウザから直接ツールを体験できます：  
👉 **[MOSSImage JSON Builder を開く](https://shnrml-spec.github.io/mossimage-json-builder/)**

オープンソース画像生成AI **MOSS-Image**（レイアウト制御・テキスト描画対応）のタスク設定JSON（`TASK_JSON`）を、直感的なキャンバス操作で作成・編集できるWebツールです。

外部ライブラリへの依存がなく、単一のHTMLファイル（`index.html`）のみで動作するため、サーバー不要でローカルのブラウザからすぐに利用できます。

### ✨ 主な機能
- **ビジュアル配置キャンバス**:
  - MOSS-Image 独自の座標系（中央原点 `abs_centralized`、フォーマット `yxyx`: `[ymin, xmin, ymax, xmax]`）に完全準拠。
  - キャンバス上でマウスドラッグして四角形（BBox）を作成・移動・リサイズするだけで自動計算。
- **画像編集（Inpaint / Edit）＆ 下絵画像の透過背景表示**:
  - 編集対象の元画像を読み込み、キャンバスの背景に「うっすら（不透明度スライダーで自由調整）」表示できます。
  - 画像ファイルのドラッグ＆ドロップ、ファイル選択、クリップボードからの貼り付け（`Ctrl + V`）にすべて対応。
  - 元画像の人物、服、看板、吹き出しの位置に合わせて正確にバウンディングボックスを重ねて配置できます。
  - 「📐 画像サイズ適用」ボタンで、元画像の解像度（Width×Height）をキャンバス解像度に一発同期。
  - 画像編集用パラメータ（`init_image`, `edit_mode: "inpaint"`, `denoising_strength`, `mask_feather`）の完全なJSON出力に対応。読み込んだ画像ファイル名が自動反映されるほか、「⚡ Colab固定スイッチ」で `/content/uploaded_input.png` への固定切替もワンタッチで行えます。
- **タグ辞書 & CSV連携**:
  - 品質・人物・構図・衣装・ポーズなどの定番タグ集（日・英）を標準内蔵。
  - タグをクリックするだけでプロンプトにワンタップ挿入。
  - 独自CSVファイルのドラッグ＆ドロップ読み込みに対応（ブラウザの LocalStorage に自動保存）。
- **日本語 → 英語 リアルタイム翻訳**:
  - プロンプト入力欄の「🌐 日→英」ボタンを押すだけで即座に英語プロンプトに変換。
  - 無料翻訳API（MyMemory）＋オフライン内蔵辞書フォールバックに対応。
- **JSONのコピー・保存・読込**:
  - ワンクリックでクリップボードへコピー、または `.json` ファイルとして保存。
  - 既存のJSONファイルを読み込んでフォームやキャンバスに復元可能。

### 🚀 使い方
1. 本リポジトリをダウンロード（またはクローン）します。
2. `index.html` をブラウザでダブルクリックして開きます。

---

## 📜 License
This project is open-sourced under the [MIT License](LICENSE).
Feel free to use, modify, and share!

### Third-Party Services Notice
- Machine translation uses the public MyMemory Translation API.
- All styles, scripts, and canvas rendering are implemented in pure vanilla HTML5/CSS/JavaScript with no external npm/CDN dependencies.
