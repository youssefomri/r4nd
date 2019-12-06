installation
------------

-   自分の環境に合ったものを以下からダウンロード＆インストール
-   [ダウンロードはこちら](https://code.visualstudio.com/download)

setup
-----

### 設定ファイルの場所

-   Users/yourname/Library/Application Support/code/User/settings.json
-   この中に設定を書いていく．

### 各種設定項目

-   キーバインド
    -   左上のcodeから設定＞キーバインド
    -   or
    -   Users/yourname/Library/Application
        Support/code/User/keybindingss.json

    の中をいじる．（多分，１回上のやり方でキーバインドを変えないと生成されないファイルだと思う）
-   テーマの変更
    -   \"workbench.colorTheme\": \"好きなテーマ\", //vscode全体のテーマ
    -   \"workbench.iconTheme\": \"好きなテーマ\",
        //ファイルアイコンのテーマ
-   文字の変更
    -   \"terminal.integrated.fontFamily\": \"好きな文字\",
        //ターミナルで使用される文字
    -   \"terminal.integrated.fontSize\": 14,
        //ターミナル内での文字の大きさ
    -   \"editor.fontSize\": 14, //エディター内での文字の大きさ
-   タブ入力の設定
    -   \"editor.renderWhitespace\": \"boundary\",
        //tabを打った時の表示方法
    -   \"editor.tabSize\": 2, //タブ文字の長さ
    -   \"editor.insertSpaces\": true, //わからんけど書いとけ
-   スクロールバーの有無（エディター内）
    -   \"editor.scrollbar.horizontal\": \"hidden\", //水平
    -   \"editor.scrollbar.vertical\": \"hidden\",　//上下
-   ターミナル起動設定 -\"terminal.integrated.cwd\":
    \"*Users/yourname*\", //起動場所
-   外観設定（追加用）
    -   \"workbench.colorCustomizations\"{この中に書く}
        -   （例） \"statusBar.background\": \"\#000000\", //
            ステータスバー背景色
-   ウィンドウのズームレベル設定
    -   \"window.zoomLevel\": -1,
-   ファイルエンコード設定
    -   \"files.encoding\": \"utf8\",
-   コードの折りたたみ **これ重要**
    -   全て折り畳む，展開

    { \"key\": \"バインドしたいキー\", \"command\":
    \"editor.unfoldAll\", //全て展開 \"when\": \"editorTextFocus &&
    foldingEnabled\" }, { \"key\": \"バインドしたいキー\", \"command\":
    \"editor.foldAll\", //全て折り畳む \"when\": \"editorTextFocus &&
    foldingEnabled\" },
    -   選択している箇所を折り畳む，展開

    { \"key\": \"バインドしたいキー\", \"command\":
    \"editor.foldRecursively\",　//一部折り畳む \"when\":
    \"editorTextFocus && foldingEnabled\" }, { \"key\":
    \"バインドしたいキー\", \"command\": \"editor.unfoldRecursively\",
    //一部展開 \"when\": \"editorTextFocus && foldingEnabled\" },
