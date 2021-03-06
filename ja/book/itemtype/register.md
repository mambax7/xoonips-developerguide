 <body>

 <div id="page">

 <div xmlns="http://www.w3.org/1999/xhtml" class="navheader">

 </div>

 <div xmlns="http://www.w3.org/1999/xhtml" class="chapter" lang="ja" id="register" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h2 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register"></a>第7章 アイテム登録</h2>

 </div>

 </div>

 </div>

 <div class="figure">

 <a id="fig.register.workflow"></a>

 <div class="figure-contents">

 <div class="mediaobject">

 <img src="../../assets/itemtype/regist-flow.gif" alt="アイテム登録画面作成の流れ" />

 </div>

 </div>

 <p class="title">

 <b>図 7.1. アイテム登録画面作成の流れ</b>

 </p>

 </div>

 <br class="figure-break" />

 <div class="figure">

 <a id="fig.register.view-parameter"></a>

 <div class="figure-contents">

 <div class="mediaobject">

 <img src="../../assets/itemtype/regist-trans.gif" alt="画面遷移と送信パラメータ" />

 </div>

 </div>

 <p class="title">

 <b>図 7.2. 画面遷移と送信パラメータ</b>

 </p>

 </div>

 <br class="figure-break" />

 <p>アイテム登録の流れは<a href="register.html#fig.register.workflow" title="図 7.1. アイテム登録画面作成の流れ">図 7.1. 「アイテム登録画面作成の流れ」</a>のとおりです．登録は以下の流れで行ないます．</p>

 <div class="orderedlist">

 <ol type="1">

 <li>

 <p>登録フォームに登録内容を入力</p>

 </li>

 <li>

 <p>登録内容確認フォームで内容の表示とシステムによる内容チェック</p>

 </li>

 <li>

 <p>登録実行</p>

 </li>

 </ol>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h2 xmlns="http://www.w3.org/1999/xhtml" class="title" style="clear: both"><a id="register.form"></a>1. 登録フォーム要求</h2>

 </div>

 </div>

 </div>

 <p>アイテムタイプモジュールはシステムの登録要求を受けて，登録フォームを作成します．登録フォームはHTMLの形式で出力します．</p>

 <p>アイテムタイプモジュールの以下の関数に登録フォーム作成処理を定義してください．システムは登録フォームが必要なときこの関数をコールバックします．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>function &lt;モジュール名&gt;GetRegisterBlock( )</p>

 <div class="itemizedlist">

 <ul type="circle">

 <li>

 <p>引数 : なし</p>

 </li>

 <li>

 <p>戻り値 : 登録フォームの HTML</p>

 </li>

 </ul>

 </div>

 </li>

 </ul>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.form.basic"></a>1.1. Basic Information の登録フォーム作成</h3>

 </div>

 </div>

 </div>

 <p>共通ライブラリの機能を呼び出して，Basic Information の登録フォームを作成します． Basic Information のフィールド毎のフォームが得られるので，その中から必要なフィールドを取り出してフォームを作成します．</p>

 <p>以下の項目も参照してください．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>xnpGetBasicInformationRegisterBlock</p>

 </li>

 </ul>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.form.detail"></a>1.2. Detail Information の登録フォーム作成</h3>

 </div>

 </div>

 </div>

 <p>Detail Information の登録フォームを作成する方法は規定しません．出力する HTML がシステムの画面構成や動作を妨げないものであれば，どのように作成しても問題ありません．共通ライブラリに用意された機能を利用して，添付ファイルや画像の登録フォームを生成できます．</p>

 <p>内容確認画面から編集フォームへ戻ってきた場合 (<a href="register.html#fig.register.view-parameter" title="図 7.2. 画面遷移と送信パラメータ">図 7.2. 「画面遷移と送信パラメータ」</a>の(3)) は，以前入力されたアイテム情報をフォームの初期値に設定するため，POST で与えられた情報をフォームの初期値に設定してください </p>

 <p>以下の項目も参照してください．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>xnpGetBasicInformationRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetPreviewRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetAttachmentRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetTextFileRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetRightsRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetIndexRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetDownloadLimitationOptionRegisterBlock</p>

 </li>

 <li>

 <p>xnpGetDownloadNotificationOptionRegisterBlock</p>

 </li>

 </ul>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.form.paramcheck"></a>1.3. パラメータチェック関数</h3>

 </div>

 </div>

 </div>

 <p>出力する HTML に Web ブラウザ上でパラメータチェックを行なうチェック関数を定義してください．JavaScript で以下の関数を定義してください．パラメータチェックを行なわない場合も定義が必要です．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>function OnSubmitItemType( form )</p>

 <div class="itemizedlist">

 <ul type="circle">

 <li>

 <p>引数 : form (登録フォームのオブジェクト)</p>

 </li>

 <li>

 <p>戻り値 : true (異常なし)，false (異常あり)</p>

 </li>

 </ul>

 </div>

 </li>

 </ul>

 </div>

 <p>フォームの Submit ボタンが押されると，OnSubmitItemType 関数がコールバックされます．アイテムタイプ独自の項目で，パラメータチェックが必要な場合はこの関数内にチェック処理を行ないます．エラーダイアログ表示などはこの関数内で行なってください．最後に，パラメータが正常な場合は true を，異常がある場合は false をかえしてください．パラメータチェックを行なわない場合は常に true をかえす処理を定義してください．</p>

 <p>false を返した場合，登録内容確認画面へは進みません．</p>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.form.reservedparam"></a>1.4. 予約済みパラメータ名</h3>

 </div>

 </div>

 </div>

 <p>システムが登録フォームで使用する (登録フォームから POST で送信する) パラメータの名前 (&lt;input&gt;タグの name 属性) は以下のとおりです．アイテムタイプモジュールが使用するパラメータが以下の名前と重複しないように注意してください．重複を避けるために Detail Information のパラメータ名にはプレフィクスとしてモジュール名を与えるとよいでしょう．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>mode</p>

 </li>

 <li>

 <p>fileID</p>

 </li>

 <li>

 <p>title</p>

 </li>

 <li>

 <p>keywords</p>

 </li>

 <li>

 <p>description</p>

 </li>

 <li>

 <p>doi</p>

 </li>

 <li>

 <p>publicationDateYear</p>

 </li>

 <li>

 <p>publicationDateMonth</p>

 </li>

 <li>

 <p>publicationDateDay</p>

 </li>

 <li>

 <p>publicationDate</p>

 </li>

 <li>

 <p>lang</p>

 </li>

 <li>

 <p>related_to</p>

 </li>

 <li>

 <p>scrollX</p>

 </li>

 <li>

 <p>scrollY</p>

 </li>

 <li>

 <p>item_type_id</p>

 </li>

 </ul>

 </div>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h2 xmlns="http://www.w3.org/1999/xhtml" class="title" style="clear: both"><a id="register.confirm"></a>2. 登録内容確認フォーム要求</h2>

 </div>

 </div>

 </div>

 <p>登録内容を確認するフォームを生成します．HTML で出力します．システムはアイテムタイプに対して以下の処理を行ないます．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>パラメータチェック関数のコールバック</p>

 </li>

 <li>

 <p>登録内容確認フォームの要求</p>

 </li>

 </ul>

 </div>

 <p>アイテムタイプモジュールの以下の関数に登録内容確認フォーム作成処理を定義してください．システムは登録内容確認フォームが必要なときこの関数をコールバックします．この関数は編集内容確認画面でも使用します．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>function &lt;モジュール名&gt;GetConfirmBlock( $item_id )</p>

 <div class="itemizedlist">

 <ul type="circle">

 <li>

 <p>引数 : $item_id (確認したいアイテムの ID．ただし登録内容確認の場合は未指定です)</p>

 </li>

 <li>

 <p>戻り値 : 内容確認画面の HTML</p>

 </li>

 </ul>

 </div>

 </li>

 </ul>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.confirm.callback"></a>2.1. パラメータチェック関数のコールバック</h3>

 </div>

 </div>

 </div>

 <p>アイテムタイプは登録内容をチェックするための PHP 関数を定義します．関数の概要は以下のとおりです．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>書式 : &lt;モジュール名&gt;CheckRegisterParameters( &amp;$msg )</p>

 </li>

 <li>

 <p>引数 : $msg (チェックしたパラメータのエラーや警告メッセージを代入する)</p>

 </li>

 <li>

 <p>戻り値 : true (異常なし)，false (異常あり)</p>

 </li>

 </ul>

 </div>

 <p>この関数内で Detail Information のパラメータチェックを行ないます．パラメータに異常があれば，その内容を示すメッセージを $msg 引数に設定し，false を返して関数を終了します．異常が無ければtrueを返します．false を返した場合，システムは登録処理実行を禁止します．$msg の内容は登録内容確認画面に出力されます．</p>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.confirm.basic"></a>2.2. Basic Information の登録内容確認フォーム作成</h3>

 </div>

 </div>

 </div>

 <p>共通ライブラリの機能を呼び出して，Basic Information の登録内容確認フォームを作成します． Basic Information のフィールド毎のフォームが得られるので，その中から必要なフィールドを取り出して組合せ，フォームを作成します．</p>

 <p>以下の項目も参照してください．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>xnpGetBasicInformationConfirmBlock</p>

 </li>

 </ul>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.confirm.detail"></a>2.3. Detail Information の登録内容確認フォーム作成</h3>

 </div>

 </div>

 </div>

 <p>以下の条件を満たしていれば，Detail Information の登録内容確認フォームの作成方法は規定しません．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>Detail Information の各フィールド値を次ページ，前ページへ送信するための &lt;input&gt; タグをつける</p>

 </li>

 <li>

 <p>送信するパラメータに予約済みパラメータ名を使用しない</p>

 </li>

 <li>

 <p>出力するHTMLがシステムの画面構成や動作を妨げない</p>

 </li>

 </ul>

 </div>

 <p>共通ライブラリに用意された機能を利用して，添付ファイルや画像の登録内容確認フォームを生成できます．</p>

 <p>以下の項目も参照してください．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>xnpGetBasicInformationConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetPreviewConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetAttachmentConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetTextFileConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetRightsConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetIndexConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetDownloadLimitationOptionConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetDownloadNotificationOptionConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetAttachmentFilenameConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetAttachmentMimetypeConfirmBlock</p>

 </li>

 <li>

 <p>xnpGetAttachmentFiletypeConfirmBlock</p>

 </li>

 </ul>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.confirm.reservedparam"></a>2.4. 予約済みパラメータ名</h3>

 </div>

 </div>

 </div>

 <p>システムが使用する( POST で送信する)パラメータの名前 (&lt;input&gt; タグの name 属性) は以下のとおりです．アイテムタイプモジュールが使用するパラメータが以下の名前と重複しないように注意してください．重複を避けるために Detail Information のパラメータ名にはプレフィクスとしてモジュール名を与えるとよいでしょう．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>title</p>

 </li>

 <li>

 <p>keywords</p>

 </li>

 <li>

 <p>description</p>

 </li>

 <li>

 <p>doi</p>

 </li>

 <li>

 <p>publicationDateYear</p>

 </li>

 <li>

 <p>publicationDateMonth</p>

 </li>

 <li>

 <p>publicationDateDay</p>

 </li>

 <li>

 <p>publicationDate</p>

 </li>

 <li>

 <p>lang</p>

 </li>

 <li>

 <p>related_to</p>

 </li>

 <li>

 <p>item_type_id</p>

 </li>

 </ul>

 </div>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h2 xmlns="http://www.w3.org/1999/xhtml" class="title" style="clear: both"><a id="register.query"></a>3. アイテム登録要求</h2>

 </div>

 </div>

 </div>

 <p>システムからの要求を受けて，アイテム登録処理を実行します．アイテムタイプモジュールの以下の関数に登録処理を定義してください．システムは登録処理が必要なときこの関数をコールバックします．登録フォームに入力された情報は $_POST 配列から取得します．登録したアイテムのアイテムIDを引数$item_idに代入してください。</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>function &lt;モジュール名&gt;InsertItem( &amp;$item_id )</p>

 </li>

 <li>

 <p>引数 : アイテムIDを受け取る変数リファレンス</p>

 </li>

 <li>

 <p>戻り値 : true (登録成功)，false (登録失敗)</p>

 </li>

 </ul>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.query.basic"></a>3.1. Basic Information の登録</h3>

 </div>

 </div>

 </div>

 <p>共通ライブラリに Basic Information 登録関数が用意されています．その関数を呼び出してください．この関数はアイテム ID を返します．このアイテム ID は Detail Information やインデックスキーワードなどと Basic Information を関連付けるために必要となります．</p>

 <p>以下の項目も参照してください．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>xnpInsertBasicInformation</p>

 </li>

 </ul>

 </div>

 </div>

 <div class="section" lang="ja" xml:lang="ja">

 <div xmlns="" class="titlepage">

 <div>

 <div>

 <h3 xmlns="http://www.w3.org/1999/xhtml" class="title"><a id="register.query.detail"></a>3.2. Detail Information の登録</h3>

 </div>

 </div>

 </div>

 <p>Detail Information を DB に登録する処理を定義します．Basic Information を登録したときに得たアイテム ID に Detail Information を関連付けて記録してください．この ID は後にアイテムの情報を参照したり編集するときに使用します．関連付けが失われると Detail Information が取り出せなくなりますので注意してください．</p>

 <p>添付ファイル，画像ファイル，テキストの登録には共通ライブラリを使用できます．</p>

 <p>Detail Information の登録方法，DB の使用，DB の種類，処理方法は規定しませんので自由に定義してください．ID との関連付けが存在するのであれば，DB を使わずファイル (CSV など) で管理してもかまいません．</p>

 <p>以下の項目も参照してください．</p>

 <div class="itemizedlist">

 <ul type="disc">

 <li>

 <p>xnpInsertBasicInformation</p>

 </li>

 <li>

 <p>xnpUpdateIndex</p>

 </li>

 <li>

 <p>xnpUpdateAttachment</p>

 </li>

 <li>

 <p>xnpUpdatePreview</p>

 </li>

 </ul>

 </div>

 </div>

 </div>

 </div>

 <div xmlns="http://www.w3.org/1999/xhtml" class="navfooter">
 </div>

 </div>
 </body>


