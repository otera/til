# logrotateメモ

RedHat系(CentOS)をベースとして記載。

## 設定ファイル

デフォルトの設定は `/etc/logrotate.conf` に存在する。  
`/etc/logrotate.d` 以下がincludeされているので、 `/etc/logrotate.d/*` にサービス毎の設定ファイルを追加すると動作される。

## sateファイル

デフォルトでは `/var/lib/logrotate/logrotate.status` に存在する。

## 定期実行

loglotate自身が自分でローテーションさせるわけでなく、cronによって `/etc/cron.daily/logrotate` のシェルスクリプトが定期実行がされる。

## オプション

### -d, –debug

デバッグモードで実行。  
ログやlogrotateのステータスファイルは変更されない。

`/usr/sbin/logrotate -d /etc/logrotate.conf`

### -f, –force

強制的にログローテーションを実行する。

### -s, –state ステータスファイル

logrotateに代替のステータスファイルを使う。  
-sを付けないときはデフォルトで `/var/lib/logrotate/logrotate.status` を参照する。

## logrotateが動作しない時

デバッグモード手動で動作はするが、cronからの起動でlogrotateされないことがある。  
その場合はSELinuxが影響していることがある。

[SELinuxでlogrotateが失敗した話 \| feedforce Engineers' blog](http://tech.feedforce.jp/selinux_and_logrotate.html)

自分が遭遇したパターンでは、logrotate設定ファイルのSELinuxコンテキストを確認した所、タイプが`user_home_t`になっていたのが原因だった。  
他設定ファイルと同様のものに変更したらcronからでも正常に動作するようになった。