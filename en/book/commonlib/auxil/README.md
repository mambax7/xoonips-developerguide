# auxil {#auxil}

| ![前のページ](../../assets/commonlib/prev.gif)  |   |  ![次のページ](../../assets/commonlib/next.gif) |
| --- | :-: | --- |

## 第14章 補足: Attachment, TextFile 系関数の $name 引数について {#14-attachment-textfile-name}

※ 1つのアイテムは，複数の Attachment/TextFile を持つことが可能です．

※ 複数の入力欄を区別するため，Attachment/TextFile 系の関数は $name 引数を持ちます．

※ $name は，予め xoops_xoonips_file_type の name カラムに登録しておく必要があります．

※ nameの登録は，モジュールインストール時に実行される `sql/mysql.sql` に INSERT 文を定義して登録できます．

以下の $name は予約済みです．

*   &#039;preview&#039;

以下の $name は既に登録済みなので，新規に登録する必要はありません．

*   &#039;readme&#039;

*   &#039;license&#039;

*   &#039;rights&#039;

| ![前のページ](../../assets/commonlib/prev.gif)  |   |  ![次のページ](../../assets/commonlib/next.gif) |
| --- | --- | --- |
|   | ![ホーム](../../assets/commonlib/home.gif)  |   |

Last updated: 2010/04/15