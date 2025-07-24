# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

XR/VR開発作品を紹介する日本語のポートフォリオサイト（静的HTML）です。ビルドツールやフレームワークは使用していません。

## Commands

### Development
- **ローカル実行**: `index.html`をブラウザで直接開く
- **ビルド/テスト/リントコマンドなし** - 純粋な静的サイト

## Architecture

### File Structure
```
├── index.html          # メインポートフォリオページ
├── styles/
│   └── styles.css      # スタイルシート
├── images/             # プロジェクト画像
└── old/               # 古いファイルのアーカイブ
```

### Key Implementation Details

1. **Navigation**: 固定ヘッダーとスムーズスクロール
   ```javascript
   // ヘッダー高さを考慮したアンカーリンクのオフセット計算
   const targetPosition = targetElement.offsetTop - 60;
   ```

2. **Work Portfolio**: クリックで展開する作品カード
   - `.work-item`コンテナ内に作品情報
   - `.work-details`は初期状態で`display: none`
   - JavaScriptで`expanded`クラスをトグル

3. **Responsive Design**: タブレット(768px以下)とモバイル(480px以下)対応

4. **YouTube Embeds**: 各プロジェクトにデモ動画を埋め込み

## Content Structure

主要なXRプロジェクト：
1. **XR Layout Planner** - PUN2マルチプレイヤー対応のMR工場レイアウトツール
2. **犬になる薬** - XRハッカソン作品のVRセラピーアプリ

両プロジェクトともUnity、Meta XR SDKを使用し、スクリーンショットと動画で紹介。