# apexfacebookmessengerbot
SalesforceのAPEXのみでFacebook Messenger Botを作成するサンプルコードです。
## 実装ステップ
+ 次の2ファイルをコピーして、APEXクラスを2つ作成します
++ fmbWebhook.apxc(トークンを書き換える場所が2箇所あります)
++ fmbMessage.apxc
+ サイト機能で外部公開用のサイトを作成します
+ 「公開アクセス設定」で、"fmbWebhook"クラスにアクセスできるようにします
++ このサンプルでは、"[サイトのURL]/services/apexrest/c/fmbWebhook"でこのクラスにHTTPでアクセスできるようになります
+ Facebook側のBotの設定ページでWebhookの認証を実行します(ここで入力する認証トークンをfmbWebhookクラスの中に記述します)
+ FacebookページとこのBotを繋ぎます(ここで入手できるページアクセストークンをfmbWebhookクラスの中に記述します)
+ Botにメッセージを送ってみます
## 注意
+ アクセスログが出ないので、うまくいかない時のデバッグが非常に難しいです
+ 少なくとも、このfmbWebhookがきちんと反応するかどうかは、crulコマンドなどで擬似的にFacebookから送られてくるであろうjsonデータを投げてあげることで確認できます
## 免責事項
