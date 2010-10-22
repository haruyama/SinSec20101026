ブロック暗号の選択肢
=================================

* `Schneier on Security: Another New AES Attack <http://www.schneier.com/blog/archives/2009/07/another_new_aes.html>`_

  * 『And for new applications I suggest that people don't use AES-256. AES-128 provides more than enough security margin for the forseeable future. But if you're already using AES-256, there's no reason to change.』

新規に用いるブロック暗号の選択肢は…?

* OpenSSL

  * aes-128系しかよさげなのがなさそう

* mcrypt(PHPでよく用いられる)

  * mcryptのrijndaelは key size = block size. つまり192,256はAESではない(AESのblock sizeは 128bit).

    * block size != 128bit だと 上記の攻撃は関係ないらしい

  * でもmcryptはTwofishやSerpentもサポートしているのでそちらのほうがよさそう

