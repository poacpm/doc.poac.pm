> English version is [here](https://doc.poac.pm/en/commands/build-commands/build.html)

# Sorry...
This page will be written soon.

<!-- ## poac build
現状のビルド順序は、未定義の状態です。
つまり、どれかのパッケージがどれかのパッケージがビルドに必要な場合、失敗する恐れがあります。
依存が循環しているときの対策を考える必要があるためです。
installコマンドの流用でいけるはずですが。

現状の案としては、lockファイルをreadすることですが、lockファイルは./depsの状態をlockしているわけではないので、難しいです。
つまり、poac.ymlの状態がlockファイルの状態を再現でき、lockファイルの状態が./depsの状態を完全に再現できるときに、初めて、lockファイルを使用してbuild順序を決定できます。
これは、実行速度としては考えもの(installコマンドの大半の処理と同じ処理を行なってしまう時がある(lockファイルが存在しない時等))なので、現状実装していません。

lockファイルが存在しなければ、installを行なっていないか、消したことになります。なので、installの実行を強制します。
また、lockファイルに書かれたtimestampが、poac.ymlと一致しないということは、現在の./depsとlockファイルの状態が一致していてるが、poac.ymlは一致していません。
（ユーザーが勝手に消し場合は異なります）
そうしたことを利用することで、うまく作ることができます。

現状、poacでのビルドしか受け付けていません。
今後、systemに、cmakeの指定等が追加されます。
そのため、installしてきたdepsをビルドしたい時は、そのディレクトリへ移動して、cmakeなりを打つことになります。 -->
