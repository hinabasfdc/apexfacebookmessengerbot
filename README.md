# apexfacebookmessengerbot
SalesforceのAPEXのみでFacebook Messenger Botを作成するサンプルコードです。

## 実装ステップ
1. 次の2ファイルをコピーして、APEXクラスを2つ作成します
  + fmbWebhook.apxc(トークンを書き換える場所が2箇所あります)
  + fmbMessage.apxc
2. サイト機能で外部公開用のサイトを作成します
3. 「公開アクセス設定」で、"fmbWebhook"クラスにアクセスできるようにします
  + このサンプルでは、"[サイトのURL]/services/apexrest/c/fmbWebhook"でこのクラスにHTTPでアクセスできるようになります
4. Facebook側のBotの設定ページでWebhookの認証を実行します(ここで入力する認証トークンをfmbWebhookクラスの中に記述します)
5. FacebookページとこのBotを繋ぎます(ここで入手できるページアクセストークンをfmbWebhookクラスの中に記述します)
6. Botにメッセージを送ってみます

## 注意
+ アクセスログが出ないので、うまくいかない時のデバッグが非常に難しいです
+ 少なくとも、このfmbWebhookがきちんと反応するかどうかは、crulコマンドなどで擬似的にFacebookから送られてくるであろうjsonデータを投げてあげることで確認できます

## 免責事項
このサンプルコードは、あくまでSalesforceのAPEXにおける機能利用の1例を示すためのものであり、コードの書き方や特定ライブラリの利用を推奨したり、機能提供を保証するものではありません。
