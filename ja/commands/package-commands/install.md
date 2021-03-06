> English version is [here](https://doc.poac.pm/en/commands/package-commands/install.html)

# Sorry...
This page will be written soon.

<!-- ## poac install

`poac install hoge` で、hogeの最新がインストールされます。
もしくは、カレントディレクトリに以下の内容を記述した`poac.yml`ファイルを作成し、
`poac install`とすることでも同様のことが可能です。
```yaml
deps:
  hoge: latest
```

許容される文法は以下です。
`poac install name=version`
`poac install name`
`poac install name1=version name2`

versionは範囲で指定することも可能です。
その際、以下のように、ダブルクオートもしくはシングルクオートで括ってください。でないとエラーになります。
`poac install "name=>=1.0.0 and <2.0.0"`

versionが指定無しの場合は、自動的に最新のものが選択されます。
つまり、`poac install name=latest`と同じ意味に解釈されます。
poac.ymlに追加される際、範囲に変換されます。(--outside option (現在未実装) 参照)
`latest`以外の場合は、そのままのバージョンでpoac.ymlに書き込まれます。

nameには、`new`コマンドで示す条件が適用されます。
半角小文字アルファベットと、半角数字, `/`, `-`, `_` のみが使用できます。
正規表現で表すなら、`^([a-z|\d|\-|_|\/]*?)=(.*)$`となります。
それ以外を使用した時は即終了します。
もちろん、versionもsetting-file.mdに示した基本文法に則していない場合はエラーです。
install時のnameに対しても処理を施して事前にthrowする。
installの場合は、リクエストをハックされないようにするため。versionは指定しないのか？-> Intervalの生成時に正規表現でチェックするため大丈夫
newコマンドも。→ ディレクトリ作成に失敗するから。
publishは、Golang側で失敗させるからOK
initは、OK
記号だけの名前のパッケージ --- とか、_ はアウト
最初や最後に記号がつくのはアウト -> /も含む -> 最初は対応済み
数字だけもアウト 0985 とか。数字から始まるのも？？？
///// や、/ は対応済み
使用可能な記号のうち、`/-`, `//`, `--`, 等の、二回以上連続して使用することはできません。

publish時と、installと、newの時にこれらのチェックが行われます


同じパッケージ名で同じバージョンのものを複数書いた場合は、警告なしに実行時依存でどちらかが優先されます。
これは、全く同じであればただの重複削除ですが、sourceが違う場合にも適用され、どちらが選択されるかは未定義です。
また、処理順序の影響で、同じパッケージのバージョン解決を複数回することになるため、実行速度に影響が出る恐れがあります。
内部では、intervalからversionに変換します。
そのため、
A: >=1.0.0 and <2.0.0
A: >=1.1.0 and <2.0.0
は、intervalとしては異なりますが、versionとしては同じかもしれません。
そのため、versionを固定化してから重複削除する必要があるので、実行速度に影響が出ます。

poac install A=1.0.0
poac install A=1.1.0
は失敗します。
なぜなら、全てのdepsで再計算するからです。
A=1.0.0と、A=1.1.0を同時にインストールしようとして失敗します。
updateしたい場合は、poac update A としてください。
(失敗しないように改善する可能性はあります。
Are you sure update A? [Y/n]
のような感じで。)

poac installを実行した後、poac.lockファイルが自動で生成されます。
このファイルは、依存関係を固めたものですが、このファイルを参照しながら、ビルドも行っていきます。
そのため、
* 依存が存在し、
* その依存がカレントディレクトリに存在しない
時、ビルド初期に自動で失敗し、以下の様なエラーを表示します。
```
Does not exists dependencies in deps. Please execute `poac install`
``` -->
