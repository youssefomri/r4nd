org-modeからJekyllに変換した際にorg内で記述した画像ファイルがJekyllに反映されない問題の解決方法
-----------------------------------------------------------------------------------------------

-   conv~mdandstoreファイルに下記のコードを追加~

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
