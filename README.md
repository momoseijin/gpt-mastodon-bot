# gpt-mastodon-bot
GPT-3のAPIを利用したmastodon向けのおしゃべり人工知能BOTです。

使い方：
Pythonのインストールをしてない人はPythonをインストールしてください。
WindowsPCであればMicrosoftStoreでPythonと検索してインストールするのが楽です。
動作確認はPython3.10で行っています。

sample.envのファイル名を.envにしてください。

https://beta.openai.com/account/api-keys

のページでAPIkeyを生成してください。

.envのファイルのkeyのところにAPIkeyを貼り付けます。

コマンドプロンプト、powershell、ターミナルなどから

pip install python-dotenv

pip install schedule

pip install mastodon.py

pip install openai

を実行します。

mastodonにBOT用のアカウントを作ってください。

setup.pyの中身を書き換えます。
mastodon_url、mastodon_login_mail、mastodon_login_passwordを自分の環境で使えるものに書き換えます。
cred_file_nameはそのままでいいでしょう。
app_nameは好きなものに変えても良いです。

python setup.py

で実行するとログインに使うファイルが生成されます。

その後

python gpt.py

で実行するとBOTが起動します。

あとはBOTにメンションをつけて話しかけてみましょう。
返事があれば成功です。
おしゃべりを楽しみましょう！

db_reset.pyについて

2023年2月22日追記：

gpt.pyの中に午前0時に文字数カウントをリセットする機能組み込んだのでdb_reset.pyはもういらないかも？

2023年7月9日追記:

依存関係がアップデートされた場合は

pip install --upgrade mastodon.py pip install --upgrade openai

を実行します。
