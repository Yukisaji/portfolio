# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

XR/VR開発作品を紹介する日本語のポートフォリオサイト（静的HTML）です。ビルドツールやフレームワークは使用していません。エンジニアポートフォリオ風のダークテーマデザインを採用。

## Commands

### Development
- **ローカル実行**: `index.html`をブラウザで直接開く
- **ビルド/テスト/リントコマンドなし** - 純粋な静的サイト

## Architecture

### File Structure
```
├── index.html          # メインポートフォリオページ
├── styles/
│   └── styles.css      # スタイルシート（GitHub風ダークテーマ）
├── images/             # プロジェクト画像とスクリーンショット
└── old/               # 古いファイルのアーカイブ
```

### Key Implementation Details

1. **Navigation**: 固定ヘッダー（60px）とスムーズスクロール
   - `scroll-padding-top: 60px`でアンカーリンクのオフセット調整
   - 背景色 `#161b22`、ボーダー `#30363d`のGitHub風デザイン

2. **Work Portfolio**: クリックで展開する作品カード機能
   - `.work-item`：通常時は33.33%幅（3列グリッド）
   - `.work-item.expanded`：展開時は100%幅
   - 展開時のスクロール調整（70pxヘッダーオフセット、500ms遅延）
   - 画像と動画を横並びで表示（各45%幅、aspect-ratio: 16/9）

3. **Visual Design Elements**:
   - 技術スタックバッジ（`.tech-badge`）: `#1f2937`背景、`#58a6ff`テキスト
   - コード風行番号表示（`.work-title::before`）
   - セクション見出しのHTMLタグ風装飾（`h1::before/after`）

4. **Responsive Design**: 
   - タブレット（768px以下）：2列表示
   - モバイル（480px以下）：1列表示

## Content Structure

収録XRプロジェクト（4作品）：
1. **VAcaAudition** - 最大100人以上同時接続可能な大規模VRプレゼンテーション空間、Photon Fusion/Vivox/AVPro Video使用
2. **ストループウォーズ** - 第17回XRハッカソン作品、認知機能訓練VRゲーム
3. **XR Layout Planner** - 第16回VRフェス作品、PUN2マルチプレイヤー対応のMR工場レイアウトツール
4. **犬になる薬** - 第16回XRハッカソン作品、VRセラピーアプリ

全作品Unity（2022/Unity6）とMeta XR SDKを使用。YouTube埋め込み動画とスクリーンショットで紹介。