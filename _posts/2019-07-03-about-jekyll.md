How to install Jekyll
---------------------

1.  Qiita jekyll install で検索 -\>
    **[here](https://qiita.com/daddygongon/items/9b7182db29861744fc79)**

2.  gem install bundler jekyll

3.  jekyll new xxx

4.  bundle exec jekyll serve

5.  立ち上がったか確認

6.  Qiitaに沿って進める

7.  daddygongon(github/jekylle~test9~)をcloneする(※他の場所で)

8.  ~data~, ~includes~, ~posts~, ~layouts~, ~sass~, assets, about.md,
    index.mdをmvする

9.  bundle update (変更毎に）

10. 自分の名前になっているか確認

How to change org-mode to Jekyll
--------------------------------

1.  Qiita org-mode Jekyll で検索 -\>
    **[here](https://qiita.com/daddygongon/items/d803d9ce6d75bef3179a)**
2.  emacs conv~mdandstore~.rb
3.  chmod a+x conv~mdandstore~.rb
4.  mv conv~mdandstore~.rb conv~mdandstore~
5.  mv conv~mdandstore~ \~/bin/
6.  conv~mdandstore~
    -   org-rubyがエラーで出たら

    <!-- -->

    -   gem install org-ruby

7.  brew upgrade rbenv ruby-build
8.  brew upgrade ruby-build
9.  brew install pandoc
10. ~posts~ の中にblog内fileが.md形式で作られているかを確認
11. htpp://localhost:4000/でblogが反映しているかを確認
    -   rm 2019-07-01-welcome-to-jekyll.markdown してもいいよ
12. END

### Questions

-   rbenv install 2.6.3
-   rbenv global 2.6.3
    -   My~help~(2.5.1)やから使えんくなった
    -   my~help~ を
        rbenv(2.6.3)に対応させるには？（my~helpはちゃんと上書きされるのか~？)
-   rm 2019-07-01-welcome-to-jekyll.markdown
