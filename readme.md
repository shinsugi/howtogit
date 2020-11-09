# git

## コミットを無かったことにしたい！
- resetコマンドでできます。
### やりかた
1. 他のブランチにコミットしたかったから、ソースの変更は残したい場合
- git reset --soft {コミットIDのようなもの}
~~~bash

> git log
commit b5fce6864b2966588371917839868c24cae6ce23 (HEAD -> master, origin/master)
Author: sugimotos <su9236nn@gmail.com>
Date:   Mon Nov 9 22:23:17 2020 +0900

    syuusei

commit e32da5d74e405a491b6f33ecb94ab21a8b77a9aa
Author: sugimotos <su9236nn@gmail.com>
Date:   Mon Nov 9 22:23:02 2020 +0900

    しゅうせい

commit 68de4f1db512fe965780004a6c513f3bf659c7e0
Author: sugimotos <su9236nn@gmail.com>
Date:   Mon Nov 9 22:22:47 2020 +0900

    initial commit

commit d494536e6e005585ec43fc82fcc9d8fe335ecd75
Author: sugimotos <su9236nn@gmail.com>
Date:   Mon Nov 9 22:17:47 2020 +0900

    initial commit ⭐️ここまで戻したい！！

> git reset --soft d494536e6e005585ec43fc82fcc9d8fe335ecd75


> git log
commit d494536e6e005585ec43fc82fcc9d8fe335ecd75 (HEAD -> master)
Author: sugimotos <su9236nn@gmail.com>
Date:   Mon Nov 9 22:17:47 2020 +0900

    initial commit
~~~
- きれいになりました

2. 変更履歴もいらない、きれいさっぱり
- git reset --hard {コミットIDのようなもの}
