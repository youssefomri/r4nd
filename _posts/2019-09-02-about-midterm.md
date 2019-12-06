とりあえずやったこと書き込む．
------------------------------

-   org-modeを使って文章（メモ，日記)を作成
    -   授業や自分の課題となることをノートやメモの様に描いていく
        -   利点（日付つけれる，段落構成できる，強調，アンダーライン，画像挿入，コード挿入，テーブル，リスト表記など）　
    -   これ一人で使う文にもいいけど，外でも見れる様にしたいよね．
    -   それにゼミのみんなとかチームのみんなと共有できたら尚いいよね.
    -   んなjekyll使ったらいいんちゃうん
        -   必要なもの（jekyll, makemd, guthub, やる気)
    -   んなとりあえずjekyll入れて先生が作ってくれてた変換ツールで変換して表示してみようや
    -   とりあず文字は見れる
-   それをみんなと共有したい -\> blogみたいな感じで毎回の記録取ろうぜ
-   myhelp edit blogですぐ呼び出せる様にしたらいいやん.
-   問題出てきたで
    -   文章，日付はいいけど画像やorg-mode独特の強調，アンダーラインというデザイン（見やすさの話）がうまくいってないよね
-   んなどうするん？
-   具体的に何が問題なん？
    -   画像に関しては
        -   orgからjekyllに変換するコマンド（後で名前確認してな）を貰ったけど，文章しかちゃんと変換されへんかった．つまり，画像の部分（ここで画像の表示のスクショでも貼ったら？）が文字のまま変換されてる．だから，元にある画像ファイルをコピーしてjekyll
            のフォルダーのコピーしなあかん．それに加えて\[\[\]\]の話もしていいかな．っていうこと．
-   結果としてはこんな感じで上手く画像を写すことができた（スクショとかでも，terminalの写真と実際のjekyllの写真でも載せといたら）
-   今後どうする?
    -   アンダーラインとか強調をうまく表示できる様にはせめてしようや．
-   それに加えて,tableの表示もうまくできたらいいよね（htmlで落とし込むとか（ここ突っ込まれそうやけど，どうやったらできそうとかいう未来像的な話)
-   参考文献とかどんな感じ?
    -   あ，それはblogの履歴見てくれた早いと思う．

今思ったけど，毎回makemdせんとこの前とのdiffだけ反映させて日付若かったら前にくるっての先に入れるっていう命令入れたら早くならへん？

IMRADで落とし込んだら？
-----------------------

-   Introduction
    -   紙ではなく自分のパソコン上にメモやノートなどを簡単に残す方法としてorg-modeがある．
    -   Jekyllを使ってBlog書いてみんなと共有したい．
    -   org-modeからJekyllへの変換をテスト
    -   画像と強調はできたが
-   Methods
    -   TDD
    -   Jekyll
    -   Org-mode
    -   Emacs
    -   Github
-   Result
    -   画像，強調はできたがアンダーライン，テーブルは上手く表示できなかった．
-   Discussion
    -   