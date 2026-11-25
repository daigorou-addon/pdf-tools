# PDF Tools

ブラウザだけで使えるPDFツール集です。インストール不要、登録不要。ファイルはこの端末の中で処理され、どこにも送信されません。

日本語 / English / 한국어 / 简体中文 / 繁體中文 / Español の6言語に対応し、ダーク／ライト表示を切り替えられます。スマホ（縦・横画面）でも使えます。

## 機能（12種類）

| ツール | できること |
| --- | --- |
| 結合 | 複数のPDFを1つにまとめる（順番の入れ替え可） |
| 抽出・削除 | ページ指定（例: `1-3,5`）で、必要なページだけ取り出す／不要なページを消す |
| 回転 | 90°右・90°左・180°。ページ指定も可能（空欄なら全ページ） |
| 並べ替え | ページ一覧を↑↓で入れ替える |
| 切り抜き | 上下左右の余白をスライダーで切り落とす |
| 圧縮 | 弱・標準・強から選んでファイルサイズを小さくする |
| ページ番号 | 位置（6方向）と形式（`1` / `1 / N`）を選んで全ページに入れる |
| 透かし | 入力した文字を斜めに全ページへ入れる（日本語可・不透明度調整可） |
| OCR（文字認識） | スキャンPDFを、検索できる文字付きのPDFにする |
| PDF→画像 | 各ページをPNG/JPEGにしてZIPで保存（倍率・ページ指定可） |
| 画像→PDF | 複数の画像を1つのPDFにする（並べ替え可。JPG/PNG/WebPなど） |
| HTML→PDF | 貼り付けたHTMLやテキストを、ブラウザの印刷機能でPDFにする |

## プライバシー

- PDFや画像などのファイルは、ブラウザの中だけで処理されます。サーバーには送信されません。
- 処理に使うライブラリ（pdf-lib、pdf.js、JSZip、Tesseract.js）はCDNから読み込みます。OCRを使う場合は、初回に言語データ（数MB）もダウンロードします。ダウンロードされるのはライブラリと言語データだけで、あなたのファイルではありません。
- HTML→PDFでは、貼り付けたHTMLの中のスクリプトは実行されません。ただし、HTMLが外部の画像やCSSを参照している場合は、それらが読み込まれます。

## 注意事項

- **圧縮**：ページを画像にして作り直します。文字の選択・検索はできなくなります。元のファイルより大きくなる場合は保存しません。
- **OCR**：初回は言語データのダウンロードが必要です。ページを画像にして文字層を付けるため、元のPDFとは別物になります。日本語は認識結果の文字の間に空白が入るため、検索で一致しないことがあります。認識の言語は、日本語＋English、English、简体中文＋English、繁體中文＋English、한국어＋English、Español から選べます。
- **切り抜き**：表示される範囲を変えるだけで、切り落とした部分のデータはファイルに残ります。見せたくない情報を隠す用途には使えません。
- **ページ番号**：数字は半角のみです。
- **HTML→PDF**：印刷ダイアログが開くので、送信先で「PDFに保存」を選んでください。
- パスワード付き（暗号化）のPDFは処理できません。パスワードの設定・解除にも対応していません。
- 動作確認はChromeで行っています。

## 使用ライブラリ

- [pdf-lib](https://github.com/Hopding/pdf-lib) — PDFの結合・分割・回転・編集
- [pdf.js](https://github.com/mozilla/pdf.js) — PDFの描画（圧縮・OCR・PDF→画像）
- [JSZip](https://github.com/Stuk/jszip) — PDF→画像のZIP作成
- [Tesseract.js](https://github.com/naptha/tesseract.js) — OCR

## リンク

- [公開ページ](https://daigorou-addon.github.io/pdf-tools/)
- [← Daigorou-Tools](https://daigorou-addon.github.io/daigorou-tools/)
- [Support Me](https://buymeacoffee.com/daigorou)

Copyright (C) daigorou-tools. All rights reserved.

---

# PDF Tools (English)

A set of PDF tools that run entirely in your browser. No installation, no sign-up. Your files are processed on your device and are never uploaded anywhere.

Available in 日本語 / English / 한국어 / 简体中文 / 繁體中文 / Español, with dark and light themes. Works on phones in both portrait and landscape.

## Features (12 tools)

| Tool | What it does |
| --- | --- |
| Merge | Combine several PDFs into one, with reorderable files |
| Extract / Delete | Keep or remove pages by range (e.g. `1-3,5`) |
| Rotate | 90° right, 90° left or 180°, for all pages or a page range |
| Reorder | Rearrange page order with ↑↓ buttons |
| Crop | Trim the top, bottom, left and right margins with sliders |
| Compress | Reduce file size with Light / Medium / Strong levels |
| Page Numbers | Add numbers to every page, with 6 positions and two formats (`1`, `1 / N`) |
| Watermark | Add a diagonal text watermark to every page (any language, adjustable opacity) |
| OCR | Turn scanned PDFs into PDFs with a searchable text layer |
| PDF to Images | Save each page as PNG/JPEG in a ZIP (scale and page range options) |
| Images to PDF | Combine images (JPG/PNG/WebP, etc.) into one PDF, with reorderable images |
| HTML to PDF | Save pasted HTML or text as PDF through the browser's print dialog |

## Privacy

- Files are processed only inside your browser and are not sent to any server.
- The libraries used (pdf-lib, pdf.js, JSZip, Tesseract.js) are loaded from a CDN. When you use OCR, language data (a few MB) is also downloaded on first use. Only libraries and language data are downloaded, never your files.
- In HTML to PDF, scripts inside the pasted HTML are not run. External images or CSS referenced by the HTML are still loaded.

## Notes

- **Compress**: Pages are rasterized and rebuilt, so text can no longer be selected or searched. If the result would be larger than the original, it is not saved.
- **OCR**: Language data must be downloaded on first use. The result is rebuilt from page images with a text layer added, so it differs from the original PDF. For Japanese, spaces appear between recognized characters, which can make searches fail to match. Available languages: Japanese + English, English, Simplified Chinese + English, Traditional Chinese + English, Korean + English, Spanish.
- **Crop**: This only changes the visible area. The trimmed-away content remains in the file, so it cannot be used to hide sensitive information.
- **Page Numbers**: Half-width digits only.
- **HTML to PDF**: A print dialog opens; choose "Save as PDF" as the destination.
- Password-protected (encrypted) PDFs cannot be processed, and setting or removing passwords is not supported.
- Tested in Chrome.

## Libraries

- [pdf-lib](https://github.com/Hopding/pdf-lib) — merge, split, rotate and edit PDFs
- [pdf.js](https://github.com/mozilla/pdf.js) — PDF rendering (compress, OCR, PDF to images)
- [JSZip](https://github.com/Stuk/jszip) — ZIP creation for PDF to images
- [Tesseract.js](https://github.com/naptha/tesseract.js) — OCR

## Links

- [Live site](https://daigorou-addon.github.io/pdf-tools/)
- [← Daigorou-Tools](https://daigorou-addon.github.io/daigorou-tools/)
- [Support Me](https://buymeacoffee.com/daigorou)

Copyright (C) daigorou-tools. All rights reserved.
