関数型言語比較
=============================

関数型特有の機能

.. list-table::
   :header-rows: 1
   :stub-columns: 1
   
   * - 言語
     - Common Lisp
     - Haskell
     - OCaml
     - F#
     - Scheme
     - Scala
     - Erlang
     - XSLT /xfy
   * - 型付け
     - 動的
     - 強い静的
     - 静的
     - 静的
     - 動的
     - 静的
     - 動的
     - 動的
   * - パターンマッチ
     - ☓
     - ◯
     - ◯
     - ◯
     - ☓?
     - ◯ 
     - ◯
     - ◯
   * - 末尾再帰の最適化
     - ◯
     - ◯
     - ◯
     - ◯
     - ◯
     - ◯
     - ◯
     - 処理系依存 [#xslt1]_
   * - ループ構文
     - ◯
     - ☓
     - △(制約多い)
     - ◯
     - ◯(あまり使わない)
     - ◯
     - ☓
     - XMLノード専用 [#xslt2]_
   * - 遅延評価
     -
     -
     -
     -
     -
     -
     -
     - ☓
   * - ストリーム
     -
     -
     -
     -
     -
     -
     -
     - ☓
   * - 破壊的代入(変数)
     - ◯
     - ☓
     - ◯
     - ◯
     - ◯
     - ◯
     - △unbound
     - ◯

.. rubric:: 脚注

.. [#xslt1] @moriyoshi: 末尾再帰の最適化は処理系によってされたりされなかったり。libxsltとxalanはしない。Saxonはする
.. [#xslt2] @moriyoshi: NodeListの列挙は組み込みのforeachでいいけど、いわゆるループは末尾再帰で書くしかなくて、そっちはスタック食いつくす

参考文献
-------------

* Google (言語名 + 破壊的代入)などでぐぐる
* `なぜＸＳＬＴ＋パイプラインか？ <http://docmgt.xoxxox.net/doc/trdwhy_plp.htm>`_
