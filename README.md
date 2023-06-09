# このwebアプリの説明

## 内容

日本の各市区町村ごとに、地名としてどのような漢字が多く使われているのかを可視化するアプリを実装しました。

最初に日本地図が表示され、都道府県をクリックするとその都道府県の詳細な地図に移行します。
そして、そこにはその都道府県単位でよく使われている漢字が表示されます。

左上の選択式ボックスにその都道府県の市区町村が一覧で表示されています。それを一つ選ぶと、その市区町村の場所が赤い丸で表示されます。checkボタンを押すと、次のページに進みます。

次のページでは、先ほど選んだ市区町村内でよく使われている漢字が表示されています。頻度が高いものほど大きな円で表示されます。
右側には、使われている漢字の類似度が高い、他の市区町村ベスト3が表示されています。市区町村の名前のところをクリックすると、今度はその市区町村がメインのページに遷移することができます。

また、チャート内の個々の漢字をクリックすると、その漢字が最もよく使われている自治体名が表示されるようになっています。その自治体名をクリックすると、ベスト3のときと同じように、その市区町村のページに遷移できます。

最初の状態に戻りたい時は左上の「Home画面に戻る」ボタンをクリックすると戻れます。





## 実装
フロントエンドはjavascript、バックエンドはpythonで作りました。
地図やバブルチャートの表示にはd3.j3というライブラリを用いています。
地名のデータは国土地理院が公表しているものを使っています。

ソースファイルの簡単な説明です。(レポジトリ内が散らかっていて見にくくなっており、申し訳ありません。)

- スタートページはindex.htmlで、そこからその他のhtmlに飛んでいくという形になっています。
- いくつかあるipynbファイルは、データ処理のために用いており、結果をcsvで出力し、javascript内で読ませています。
- dataフォルダの中に各都道府県の地図が格納されています。
- prefecturesフォルダの中には、各都道府県ごとの地名情報などのデータが入っています。



## 注意点
未実装の部分が多く、一部の県でのみ正しく動く仕様になっています。
神奈川県と栃木県は完成しているので、利用する際にはその２県を選んでいただけると良いと思います。

また、選んだ市区町村によってはベスト３が表示されなかったりすることがあります。その際は他の場所を選択し直してください。

全体的に完成度が低くなってしまっておりますが、ご承知おきいただけますと幸いです。
