> English version is [here](https://doc.poac.pm/en/commands/manifest-commands/update.html)

# Sorry...
This page will be written soon.

<!-- ## poac update
updateするには、updateコマンドを使用します。
./depsの内容を大幅に書き換えられていたら？？？ -> cuurent_nameから、for_loopできる。その際、srcがgithubでなければ良い
依存関係から後に外れたもの。
A -> B -> C だった時に、installを行なっていて、
Bが、Cに依存しなくなり、Aの依存範囲内に入っていたら、更新される。
この際、Cは完全に無視されてしまう。
そのため、定期的に./depsをcleanした方がよい。
そうした、依存関係から外れたパッケージを削除してくれるコマンドを考え中のため、今後実装される。
もちろん、B:1.0がB:2.0になった場合には、B:1.0が削除されてからB:2.0がインストールされるため、上記のようなコマンドはこのケースには不要である。

poac.ymlから、poac.lockが再現できたとしても、そこで終了とはならない。
何故なら、lockファイルは、./depsの状態を表現している訳ではないからである。
ユーザーによってファイルが削除されたり追加されたりしている可能性を考慮する必要があるからだ。
そのため、如何なる場合においても、lockファイルは無視し、poac.ymlによって生成された依存木と、./depsを比較する。
lockは古い可能性もあるからだ。
その際、違いがあれば、replaceされ、lockファイルが更新される。

各バージョンの状態に関しては、npm outdatedに則って、
Current, Wanted, Latest
の３つの状態で表される。
Currentが、現在インストールされているバージョン
Wantedが、semverで指定した範囲の条件を満たす中での最新のバージョン
Latestが、そのパッケージでの最新のバージョン

A -> Current: 1.0.0, Wanted: 0.5.0, Latest: 1.0.0
という状態で、poac update Aを実行した時、Aは、0.5.0にdowngradeされる。
つまり、updateは、更新であり、upgradeとdowngradeの両方を行うことができる。

また、A, B, Cに依存していたとき、
./depsに、AとBしか入っておらず、poac updateを実行したなら、Cがインストールされます。
これは、Cがdepsに存在しないことと、Cが存在していて新しいバージョンが存在することが同じ解釈になるためです。

### 個別のupdate (現在未実装)

### 依存の依存 (現在未実装)
依存の依存に対して、update指定は可能か？？？
可能です。
その場合は、依存の依存とそれ以降の依存のみが変更の対象になり、それ以外は評価されません。
例えば、
poac.ymlに
A: 1.0.0
として、
A -> B -> C
となっており、
`poac update B`とすると、BとCが評価されます。

### --outside option (現在未実装)
--outsideを指定すると、poac.ymlに指定した範囲外に検証範囲を広げてくれます。
つまり、Wantedではなく、Latestのバージョンにupdateされるということです。
実行時に変更があれば、poac.lockだけでなく、poac.ymlも書き換えられます。
(--outsideが付いてない場合で更新が存在する場合は、poac.lockが書き換えられます)
一つのバージョンではなく、マイナーの範囲を許す範囲に設定されます。(npmでいう^(caret)に近い動作)
poac.ymlに、
A: ">1.0.0 and <=2.0.0"
A -> Current: 2.0.0, Wanted: 2.0.0, Latest: 3.0.0
だとすると、
`poac update A --outside`
で、poac.ymlは、
A: ">=3.0.0 and <4.0.0"
に書き換えられます。
先ほど、npmでいう^(caret)に **近い** 動作と表現したのは、
`>=0.0.1 and <0.0.2` とnpmだとなるのに対し、
--outside optionだと、
`>=0.0.1 and <1.0.0` となるからです。
(poacは、一番左のmajorバージョンしか見ない。つまり、majorバージョンのみの固定化を行う)

### 指定のバージョンにupdateしたい
poac.ymlの範囲を調節してください。 -->
