org-modeからJekyllに変換した際にorg内で記述した画像ファイルがJekyllに反映されない問題の解決方法
-----------------------------------------------------------------------------------------------

**conv~mdandstoreファイルに下記のコードを追加~**

> ``` {.example}
> $target2 = File.join ENV['HOME'],'.my_help/img/' #各自のディレクトリ名に変更
> $jekyll_img_path = File.join ENV['HOME'],'Final/r4nd/img/' #各自のディレクトリ名に変更
> ```

[解説]{.underline}

-   \$target2は.my~helpディレクトリに画像専用のディレクトリを作りそこまでのpathとする~．
-   Jekyll~imgpathはJekyllのディレクトリ内に画像専用ディレクトリを作り~，そこまでのpathとする．

> ``` {.example}
> img = line.match /\[\[file:(.*)\/(.*)\]\]/
> if img != nil
>   img_path = $target2 + img[2]
>   puts 'copy_image_name -> '.yellow + img[2].green
>   FileUtils.cp(img_path, $jekyll_img_path)
> end
> ```

[解説]{.underline}

-   orgファイルを１行ずつ読み，画像ファイルの名前だけを抽出．(img\[2\])
-   その中身を.my~help内のimgディレクトリからJekyll内のimgディレクトリへコピーする~．

[結果]{.underline}

!\[\]({{site.baseurl}}/img/png~result~.png)

Jekyll(Theme:cayman)でorg-mode編集日時の反映方法
------------------------------------------------

**JekyllのDirectory内にblog.mdを作り以下のコードを入力する**

> ``` {.example}
>    <h1>Latest Posts</h1>
> <ul>
> {% for post in site.posts %}
> <li>
> <h2><a href="{{ post.url | relative_url }}">
> {{ post.date | date: '%Y/%m/%d-%A' }} : {{ post.title }}
> </a></h2
> <p>{{ post.excerpt }}</p>
> </li>
> {% endfor %}  
> </ul> 
> ```

[結果]{.underline}

!\[\]({{site.baseurl}}/img/date~result~.png)

\[追記\]conv後に生成されるtmpファイルと編集で削除した記事をhtmlに反映させない様にする方法
-----------------------------------------------------------------------------------------

> ``` {.example}
> FileUtils.rm(Dir.glob('/Users/youssefomri/Final/r4nd/_posts/*'))
> ```

-   自分のjekyllディレクトリにある~posts内の~.mdファイルを削除する.
