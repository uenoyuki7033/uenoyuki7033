上野用メモ　publicなので、記載する情報に注意すること

---

# OS old ver download link
- vinelinux
http://beta.vinelinux.org
- centos
https://wiki.centos.org/Download

- tcltls lib
https://core.tcl-lang.org/tcltls/uv
---

８．６混在してインストールさせる場合
（念のため、ｘ８６のバイナリは開発機でコンパイルして持ってい行ったほうがよさそう）
./configure --prefix=/opt/tcl86
make install
export PATH=/opt/tcl86/bin:$PATH
export LD_LIBRARY_PATH=/opt/tcl86/lib:$LD_LIBRARY_PATH

これにより、Tcl/Tk 8.6のバイナリとライブラリが使用可能になります。
また、Tcl/Tk 8.4のバイナリとライブラリも引き続き利用可能です。


---
# cat /etc/redhat-release
CentOS release 5.10 (Final)
2. リポジトリファイルの更新
以下のリポジトリファイルを開きます。

# vi /etc/yum.repos.d/CentOS-Base.repo
既に指定されている baseurl の行はすべてコメントアウトして各セクションへ以下の行を追加します。

[base]
baseurl=http://archive.kernel.org/centos-vault/5.10/os/$basearch/
[updates]
baseurl=http://archive.kernel.org/centos-vault/5.10/updates/$basearch/
[extras]
baseurl=http://archive.kernel.org/centos-vault/5.10/extras/$basearch/
[centosplus]
baseurl=http://archive.kernel.org/centos-vault/5.10/centosplus/$basearch/
[contrib]
baseurl=http://archive.kernel.org/centos-vault/5.10/contrib/$basearch/


[2ページ目](readme2.md)

[マークダウン記述](マークダウン記述)

-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-
