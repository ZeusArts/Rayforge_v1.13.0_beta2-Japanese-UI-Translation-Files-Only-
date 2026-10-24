# Rayforge v1.13.0-beta2 Japanese UI Translation Files

レーザー加工・オープンソース・ソフトウェア **Rayforge** 用の日本語翻訳ファイルです。  
このリポジトリには、UI の大部分を日本語化するためのファイルが含まれています。

---

## ⚠️ 免責事項

- これらの翻訳ファイルは **本家 Rayforge とは一切関係のない個人制作** のものです。
- **各自、自己責任でご使用ください。**
- 翻訳箇所が膨大なため、すべてを細かくチェックしきれていません。
- 継続的な修正や、確実な修正対応をお約束することはできません。
- より適切な表現があれば Issue やコメントで教えていただけると助かります。
- この翻訳ファイルをベースに各自で自由に編集・改変していただいて構いません。

---

## 🔗 公式リンク

公式 Rayforge 本体：[GitHub - barebaric/rayforge](https://github.com/barebaric/rayforge)

---

## 📥 インストール方法

公式リポジトリから Rayforge をインストールした直後に、ルートディレクトリ内の以下のフォルダ構造でファイルを配置し、Rayforge を再起動すると、言語設定に **「Japanese」** が表示されるようになります。

> ※ Linux 環境でも Windows 環境でも、Rayforge のルートディレクトリ内のフォルダ・ファイル構造はほぼ同じです。どちらでもご使用いただけます。

---

## 📁 フォルダ構造・配置場所

```
rayforge/
├── locale/
│   └── ja/
│       └── LC_MESSAGES/
│           └── rayforge.mo
└── builtin_addons/
    ├── rayforge-addon-ai-workpiece/
    │   └── locale/ja/LC_MESSAGES/ai_workpiece_generator.mo
    ├── rayforge-addon-automation/
    │   └── locale/ja/LC_MESSAGES/automation.mo
    ├── rayforge-addon-laser/
    │   └── locale/ja/LC_MESSAGES/laser_essentials.mo
    ├── rayforge-addon-post/
    │   └── locale/ja/LC_MESSAGES/post_processors.mo
    ├── rayforge-addon-print-and-cut/
    │   └── locale/ja/LC_MESSAGES/print_and_cut.mo
    └── rayforge-addon-sketcher/
        └── locale/ja/LC_MESSAGES/sketcher.mo
```

---

## 📄 同梱ファイル一覧

| ファイル名 | 対象 |
|------------|------|
| `rayforge.mo` / `rayforge.po` | 本体 UI（メニュー、設定、ダイアログ等） |
| `laser_essentials.mo` / `laser_essentials.po` | レーザー機能（カット、彫刻、材質テスト等） |
| `sketcher.mo` / `sketcher.po` | スケッチャー（図形描画、制約等） |
| `automation.mo` / `automation.po` | 自動化機能 |
| `ai_workpiece_generator.mo` / `ai_workpiece_generator.po` | AI ワークピース生成 |
| `post_processors.mo` / `post_processors.po` | ポストプロセッサー |
| `print_and_cut.mo` / `print_and_cut.po` | 印刷 & カット機能 |

> **注意**: `.mo` ファイルが Rayforge 本体で読み込まれます。`.po` ファイルは人間が編集するためのソースファイルです。

---

## 🛠 翻訳ファイルを自分で修正したい場合

1. `.po` ファイルを **Notepad++**、**VS Code**、**Poedit** 等で編集
2. `.mo` 形式に再ビルド（コンパイル）する

```bash
# 一括コンパイル（推奨）
bash scripts/update_translations.sh --compile-only

# または Python で手動
python -c "import polib; from pathlib import Path; [polib.pofile(str(p)).save_as_mofile(str(p.with_suffix('.mo'))) for p in Path('.').rglob('locale/ja/LC_MESSAGES/*.po')]"
```

> **注意**: `.mo` ファイルに変換しないと Rayforge 本体に翻訳修正個所が読み込まれないのでご注意ください。
> *(正確には Rayforge メインプログラムで読み込まれているのは `.mo` ファイルだけであり、`.po` 形式ファイルは人間が編集するためのものです。)*

---

## MSYS2 UCRT64 で.po形式ファイルを.moファイルに変換する方法（場合によっては一番簡単な方法）
    MSYS2 UCRT64 ターミナルで、Rayforgeリポジトリのルートで実行

    1. MSYS2 UCRT64 ターミナルを開く
    - スタートメニュー → 「MSYS2 UCRT64」 を起動
    - PowerShell / CMD / 通常の bash ではダメです

    2. リポジトリルートに移動
    bash
    cd /c/Users/xxxxxxx/rayforge

    ※ あなたの環境では C:\Users\xxxxxxx\rayforge がリポジトリルートです

    3. 実行コマンド（どちらか一つ）

    方法A：標準スクリプト（最推奨・エラー時も詳細が出る）
    bash
    bash scripts/update_translations.sh --compile-only


    方法B：Pythonワンライナー（スクリプトが壊れてる場合の保険）
    bash
    python -c "import polib; from pathlib import Path; [polib.pofile(str(p)).save_as_mofile(str(p.with_suffix('.mo'))) for p in Path('.').rglob('locale/ja/LC_MESSAGES/*.po')]; print('完了')"




    実行確認チェックリスト

    bash
    1. 正しい場所にいるか確認
    pwd
    → /c/Users/xxxxxxxxx/rayforge

    2. 対象ファイルが見えているか確認
    find . -name ".po" -path "/ja/LC_MESSAGES/*" | head -10

    3. 実行
    bash scripts/update_translations.sh --compile-only

    4. 完了確認
    find . -name ".mo" -path "/ja/LC_MESSAGES/*" | wc -l
    → 7 なら成功（rayforge + 6アドオン）

## 📝 翻訳者

**Kleber.Kato - ZeusArts_Japan**

---

## 📄 ライセンス

この翻訳ファイルは個人制作物です。自由に使用・改変・再配布していただいて構いません。
