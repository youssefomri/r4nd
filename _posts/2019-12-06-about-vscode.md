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

    以下の項目をkeybinding,jsonへ記述していく．

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
    -   ターミナル起動設定
        -   \"terminal.integrated.cwd\": \"*Users/yourname*\",
            //起動場所
    -   外観設定（追加用）
        -   \"workbench.colorCustomizations\"{この中に書く} -（例）
            \"statusBar.background\": \"\#000000\", //
            ステータスバー背景色
    -   ウィンドウのズームレベル設定
        -   \"window.zoomLevel\": -1, //デフォルト0
    -   ファイルエンコード設定
        -   \"files.encoding\": \"utf8\",

めんどくさがりなあなたのために
------------------------------

私の設定を晒します．

以下をsettings.jsonへコピペするといい感じになります．

**変更項目あり**

``` {.example}

{
    "editor.minimap.enabled": false,
    //"workbench.editor.swipeToNavigate": true,
    "editor.renderWhitespace": "boundary",
    "editor.renderIndentGuides": true,
    "editor.quickSuggestions": true,
    "editor.tabSize": 2,
    "editor.insertSpaces": true,
    "files.trimTrailingWhitespace": true,
    "workbench.statusBar.visible": true,
    "workbench.activityBar.visible": false,
    "workbench.editor.enablePreviewFromQuickOpen": false,
    "workbench.editor.enablePreview": false,
    "workbench.startupEditor": "none",
    "window.zoomLevel": -1,
    "terminal.integrated.fontFamily": "Source Code Pro for Powerline",
    "terminal.integrated.fontSize": 13,
    "editor.fontSize": 13,
    "workbench.colorTheme": "One Dark Pro",
    "editor.cursorStyle": "block",
    "files.encoding": "utf8",
    "extensions.autoUpdate": true,
    "editor.formatOnPaste": true,
    "editor.formatOnType": true,
    "window.restoreWindows": "one",
    "editor.renderLineHighlight": "gutter",
    "workbench.tree.indent": 5,
    "workbench.tree.renderIndentGuides": "none",
    "editor.folding": true,
    "editor.wordWrap": "on",
    "workbench.editor.tabSizing": "shrink",
    "workbench.colorCustomizations": //追加項目（外観）
    {
        "statusBar.background": "#000000", // ステータスバー背景色
        "statusBar.foreground": "#8FBE8F", // ステータスバー前景色
        "statusBar.border": "#8FBE8F", // ステータスバーの境界線
        "sideBar.background": "#000000", // サイドバーの背景色
        "sideBar.foreground": "#8FBE8F", // サイドバーの前景色
        "sideBar.border": "#8FBE8F", // サイドバーの境界線
        "activityBar.background": "#000000", // アクティビティバーの背景色
        "activityBar.foreground": "#8FBE8F", // アクティビティバーの前景色
        "activityBar.border": "#8FBE8F", // アクティビティバーの境界線
        "editor.background": "#000000", // エディタ背景色
        "scrollbarSlider.background": "#8FBE8F", // スクロールバーの色
        "scrollbarSlider.hoverBackground": "#8FBE8F", // 移動中のスクロールバーの色
        "editorGroupHeader.tabsBackground": "#000000", //"タブの背景色",
        "tab.activeForeground": "#8FBE8F", //""アクティブなタブの文字色",
        "tab.border": "#000000",
        "tab.unfocusedActiveBorder": "#000000",
        "tab.activeBorder": "#8FBE8F",
        "titleBar.border": "#8FBE8F",
        "tab.inactiveBorder": "#8FBE8F",
        "tab.inactiveBackground": "#000000", //"非アクティブな色の背景色",
        "tab.activeBackground": "#000000", //"非アクティブな色の背景色",
        "tab.inactiveForeground": "#888888", //"非アクティブなタブの文字色",
        "terminal.border": "#8FBE8F",
        "panel.border": "#8FBE8F",
        "panelInput.border": "#8FBE8F",
        "panelTitle.activeBorder": "#8FBE8F",
        "menu.border": "#8FBE8F",
        "terminal.foreground": "#8FBE8F",
        "focusBorder": "#8FBE8F",
        "window.activeBorder": "#8FBE8F",
        "window.inactiveBorder": "#8FBE8F",
        "editorGroup.border": "#8FBE8F",
        "editorLineNumber.foreground": "#8FBE8F",
    },
    "workbench.iconTheme": "vs-minimal",
    "workbench.panel.defaultLocation": "bottom",
    "workbench.editor.showTabs": true,
    "editor.smoothScrolling": true,
    "editor.scrollbar.horizontal": "hidden",
    "editor.scrollbar.vertical": "hidden",
    "terminal.integrated.scrollbar.horizontal": "hidden",
    "terminal.integrated.scrollbar.vertical": "hidden",
    "terminal.integrated.experimentalRestore": true,
    "editor.fastScrollSensitivity": 1,
    "editor.scrollBeyondLastColumn": 1,
    "editor.scrollBeyondLastLine": false,
    "terminal.integrated.fontWeightBold": "bold",
    "terminal.integrated.cwd": "/Users/youssefomri/",
    "workbench.list.horizontalScrolling": false,
    "workbench.list.verticalScrolling": false,
    "editor.cursorSmoothCaretAnimation": true,
    "editor.cursorBlinking": "solid",
    "terminal.integrated.cursorBlinking": false,
    "editor.formatOnSave": true,
}

```

下から８行目

(※) \"terminal.integrated.cwd\": \"*Users/youssefomri*\",

ここだけ自分のパスにして下さい.

**変更による動作不良に関しての責任は一切負いません**

すいません，ただ言ってみたかっただけです．

\[追記\] emacsとの比較と導入/操作方法
-------------------------------------

### EmacsとVScodeの比較　

  ---------------- ------------------------------------ --------------------------------------------
                   Emacs                                VScode
  ビジュアル       なんか，シンプルすぎる               windowを何個も出せるので見た目はかっこいい
  カスタマイズ性   簡単に拡張できないのでめんどくさい   様々な拡張性を持ち，カスタマイズ性に富む
  org-mode         とても使いやすい                     拡張機能にorg-modeがあるが使い辛い
  ---------------- ------------------------------------ --------------------------------------------

### 導入/操作方法

以前，Emacsを使っていたのでVScodeでもEmacsのキーバインドを使いたいという要求が現れた．そこで，VScodeの拡張機能を使いEmacsのキーバインドを導入した．

-   導入方法

    -   VScode内にある拡張機能のアイコンをクリック
    -   入力フォームにEmacs
        Keymapと入力するとダウンロードとインストールが完了する．

-   操作方法(Emacs Keymap無し)

    -   カーソル移動 -\> ctl + p, f, b, n,
    -   ウィンドウの切り替え -\> ctl + 1,2,3,...
    -   ターミナルへ移動 -\> command + \`
    -   コピー，ペースト -\> command + c / command + v
    -   セーブ -\> command + s
    -   undo -\> command + z

-   操作方法(Emacs Keymap有り） **上記との差異のみ記述**

    -   セーブ -\> ctl + x \> ctl + s
    -   切り取り，貼り付け -\> ctl + k \> ctl + y

    簡単な操作方法は以上になりますが，拡張機能のEmacs
    Keymapを見てもらうと，Emacsのキー操作がどこまで対応しているかを表で記述していますので，そこを参照してもらうとわかりやすいと思います．

    又，デフォルトのキー操作を自分好みに変更できるので，設定 \>
    キーバインド設定から変更して下さい．

追加があれば追記していきます．

他はググって下さい.

以上
