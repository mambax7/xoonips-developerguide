## 12\. bool xnpGetDownloadNotificationOptionEditBlock( string dirname, int option ) {#12-bool-xnpgetdownloadnotificationoptioneditblock-string-dirname-int-option}

添付ファイルのダウンロード通知を編集するフォームを生成します．アイテムタイプがアイテム編集画面を作成する際に使用します．

dirname引数で添付ファイルが属するモジュールのフォルダ名を指定します．option引数で，通知の初期値を指定します．1で通知する，0で通知しない，を意味します．

$_POST[&#039;attachment_dl_notify&#039;]が定義されている場合はoption引数の値は無視されます．

### 12.1\. 内部で参照する $_POST 変数 {#12-1-post}

*   $_POST[&#039;attachment_dl_notify&#039;]

### 12.2\. 送信データ {#12-2}

*   $_POST[&#039;attachment_dl_notify&#039;]