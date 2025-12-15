# スニペットくん ver1.0（暫定版）

RPGツクールMZ向け  
**VSCodeスニペット生成支援ツール（HTML + JavaScript 単一ファイル）**

---

## 概要

**スニペットくん** は、  
RPGツクールMZで使用する **制御文字** および **Text2Frame タグ** を  
**VSCode用スニペット形式（JSON）** に一括生成するための支援ツールです。

- HTML + JavaScript 単一ファイル
- ブラウザでそのまま動作
- インストール不要
- localStorage による保存・読込対応
- 項目数・文言・順序を固定した安全設計

---

## 公開URL（GitHub Pages）

以下のURLから、**ダウンロード不要で直接起動**できます。

👉 https://okarin0083.github.io/snippet_kun/

---

## 対応項目（固定仕様）

| カテゴリ | 項目数 |
|---|---|
| 制御文字（RPGツクールMZ） | 12 |
| Text2Frame タグ | 43 |
| **合計** | **55** |


## 使い方

### 1. 起動方法

#### 方法A：ブラウザ版（推奨）
- 上記 GitHub Pages のURLを開くだけ

#### 方法B：ローカル実行
1. `snippet_kun_ver1.0.html` をダウンロード
2. ブラウザで開く

---

### 2. 画面構成

- 表は中央配置
- 横幅は内容最大に自動追従
- 以下2カテゴリを表示
  - 制御文字（MZ）
  - Text2Frame タグ

---

### 3. 編集可能な項目

編集できるのは **短縮ワード（prefix）** のみです。

- body（本文）
- description（説明）
- 項目数・順序  
- 「編集」ボタンで再編集可能

---

### 5. 行操作

- **行追加**  
  - 表の右下ボタン
- **行削除**  
  - 各行右側の削除ボタン

※ 行追加・読込後もキー操作は自動で有効になります。

---

## キー操作仕様（重要）

| 操作 | 動作 |
|---|---|
| Tab | 右のセルへ移動 |
| Enter | 下のセルへ移動 |
| Shift + Enter | セル内改行 |
| IME確定時のEnter | 無視（移動しない） |

---

## 保存 / 読込

- **保存**：現在の状態を localStorage に保存
- **読込**：保存済みデータを復元

※ ブラウザを閉じても内容は保持されます。

---

## 出力（VSCodeスニペット）

### 出力結果

- 「出力結果」ボタンで一括生成
- JSON形式で表示
- 「一括コピー」対応

### 出力フォーマット

## 想定用途

- RPGツクールMZで使用する制御文字の入力補助
- Text2Frame プラグイン利用時のタグ入力効率化
- VSCode用スニペット（JSON）の一括生成・再生成
- 複数環境（PC入替・再インストール時）でのスニペット管理
- タグ・制御文字の「一覧＋編集＋出力」を一画面で完結させたい場合

本ツールは  
**「覚えなくていい」「コピペミスを減らす」「再生成できる」**  
ことを主目的としています。

---

## ⚠️注意事項

- 本ツールは **項目固定型ツール** です  
  - 項目数・文言・順序は仕様として固定されています
- ブラウザの localStorage を使用します  
  - シークレットモードでは保存されません
- 本ツールの使用によって生じたいかなる不具合・損害についても、作者は責任を負いません
- RPGツクールMZ本体および各種プラグインの仕様変更により、将来的に出力内容が適合しなくなる可能性があります

---

## License

MIT License

Copyright (c) 2025 okarin0083

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE  
SOFTWARE.


```json
{
  "カテゴリ名": {
    "prefix": "短縮ワード",
    "body": [
      "本文1行目",
      "本文2行目"
    ],
    "description": "説明文"
  }
}

