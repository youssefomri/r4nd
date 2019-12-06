Installation
------------

-   自分の環境に合ったものを以下からダウンロード＆インストール
-   [ダウンロードはこちら](https://code.visualstudio.com/download)

Setup
-----

### 設定ファイルの場所

-   Users/yourname/Library/Application Support/code/User/settings.json

この中に設定を書いていく．

### ターミナルについて

-   ターミナルは\[ command + \` \]で呼び出せる(変更可能)．

もう一度入力すると消える．

### 各種設定項目

-   keybindings.json 編

    -   左上のCode(Appleマークの右)から基本設定 \> キーバインド設定

    or

    -   Users/yourname/Library/Application
        Support/code/User/keybindings.json の中をいじる.

    **(※)１度キーバインド設定から変更を加えないと生成されないファイルかも**

    -   コードの折りたたみ設定

        -   全て折り畳む，展開

        ``` {.example}
        {
          "key": "バインドしたいキー",
          "command": "editor.unfoldAll", //全て展開
          "when": "editorTextFocus && foldingEnabled"
         },
        {
          "key": "バインドしたいキー",
          "command": "editor.foldAll", //全て折り畳む
          "when": "editorTextFocus && foldingEnabled"
        },
        ```

        -   選択している箇所を折り畳む，展開

        ``` {.example}
         {
           "key": "バインドしたいキー",
           "command": "editor.foldRecursively",　//一部折り畳む
           "when": "editorTextFocus && foldingEnabled"
        },
        {
           "key": "バインドしたいキー",
           "command": "editor.unfoldRecursively", //一部展開
           "when": "editorTextFocus && foldingEnabled"
         },
        ```

    -   正直，基本設定 \> キーバインド設定から変更した方が早い．

        勝手に.jsonに書いてくれるし．

-   settinsgs.json 編

    Code \> 基本設定 \> 設定 からも変更可

    以下をsettings.jsonに記述していく．

    -   テーマの変更
        -   \"workbench.colorTheme\": \"好きなテーマ\",
            //vscode全体のテーマ
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
        -   \"workbench.colorCustomizations\"{この中に書く} -（例）
            \"statusBar.background\": \"\#000000\", //
            ステータスバー背景色
    -   ウィンドウのズームレベル設定
        -   \"window.zoomLevel\": -1, //デフォルト0
    -   ファイルエンコード設定
        -   \"files.encoding\": \"utf8\",

追加があれば記述していきます．

後はググって下さい.

以上
