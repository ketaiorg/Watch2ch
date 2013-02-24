# このプログラムについて

Watch2chは、PHPで作られた2chの監視を目的としたプログラムです。  
指定したスレの勢いをチェックし、閾値を超えた場合にスレッドの内容を出力します。  
（cronに設定することでこれをメールさせることができます）  
実行環境にはLinux+PHP5.1以降を推奨しています。  

* @author 松井 健太郎 (Kentaro Matsui) <info@ke-tai.org>
* @copyright ke-tai.org
* @license BSD


# 実行方法

* サンプルのconfigをコピーして設定ファイルを作成します  
`$ cp sample.conf my_setting.conf`  
`$ vi my_setting.conf`  

* 設定項目は以下の通りです  
 - BoardName : URLに使われている板の識別名(http://\*.2ch.net/に続く文字)を設定します  
 - Keyword : 対象としたいスレ名を正規表現で指定します（対象が複数ある場合は先に見つかったものを使用します）  
 - BorderForces : 勢いの閾値を出力します  
 - OutputNum : 閾値を超えた場合にレスを幾つ出力するかを指定します

* 次のように実行します  
`./watch_2ch my_setting.conf`  

閾値を超えていればレスが出力され、そうでなければ何も出力されません  

