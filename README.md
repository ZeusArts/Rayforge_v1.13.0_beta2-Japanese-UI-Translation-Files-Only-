# Rayforge_v1.13.0_beta2-Japanese-UI-Translation-Files-Only-
これはレーザー加工・オープンソース・ソフトウェアであるRayforge用の日本語翻訳ファイルです。 このリポジトリ内にはUIの大部分を日本語化する為のファイルが置いてあります。

GeminiとNemotronで様々な手を尽くして莫大な数のコードを日本語化しましたが、
翻訳個所が莫大な為、すべてに目を通して細かくチェックは出来ないので、
一応極力目を通してやりましたがこれでも個人で努力し尽くしたつもりですが、
一部の翻訳個所で誤りがあるかも知れませんが、ご了承ください。

このファイルを公式のリポジトリからファイルをインストールした直後に、
ルートディレクトリ内の以下のフォルダー内にファイルを収めることで、
再起動後に言語設定項目内に「Japanese」の選択が出来るようになります。
＊（この翻訳ファイルはLinux環境でもWindows環境でもRayforgeのルートディレクトリ内の
フォルダーとファイル構造はほぼ一緒ですので、どちらでもご使用いただけます。）

フォルダー構造・ファイルの配置場所：

　rayforge/locale/ja/LC_MESSAGES/rayforge.mo
    rayforge/builtin_addons/rayforge-addon-ai-workpiece/locale/ja/LC_MESSAGES/ai_workpiece_generator.mo
    rayforge/builtin_addons/rayforge-addon-automation/locale/ja/LC_MESSAGES/automation.mo
    rayforge/builtin_addons/rayforge-addon-laser/locale/ja/LC_MESSAGES/laser_essentials.mo
    rayforge/builtin_addons/rayforge-addon-post/locale/ja/LC_MESSAGES/post_processors.mo
    rayforge/builtin_addons/rayforge-addon-print-and-cut/locale/ja/LC_MESSAGES/print_and_cut.mo
    rayforge/builtin_addons/rayforge-addon-sketcher/locale/ja/LC_MESSAGES/sketcher.mo
	
	日本語翻訳ファイルリスト：
	
	rayforge.mo
    rayforge.po
    ai_workpiece_generator.mo
    ai_workpiece_generator.po
    automation.mo
    automation.po
    laser_essentials.mo
    laser_essentials.po
    post_processors.mo
    post_processors.po
    print_and_cut.mo
    print_and_cut.po
    sketcher.mo
    sketcher.po
	
	各個人で翻訳ファイルを修正したい場合は、.po形式ファイルをNotepad++やコードエディタで編集後に、.mo形式に再ビルドする必要性があります。
	.mo形式に変換しなければRayforge本体に翻訳修正個所が読み込まれないのでご注意ください。
	*(正確にはRayforgeメインプログラムで読み込まれているのは.moファイルだけであり、.po形式ファイルは人間が編集するためのものです。)
	
	
	翻訳者：Kleber.Kato - ZeusArts_Japan
