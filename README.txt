概要：
AWS費用削減シートに記載する内容をboto3で取得するコード
VScode+での動作を想定しています
output.txtに記載されている情報が取得できます

利用方法：
=========== devコンテナ起動　===========
1: このリポジトリをgit clone後、VScodeで開く
2 :左下の「><」マークをクリック
3: 「コンテナーで再度開く」をクリック

=========== AWS PROFILE 設定 ===========
1: ~/.aws/config と ~/.aws/credentials を設定
2: ターミナルで以下コマンド実行（ii-devはprofile名です、適宜変更してください）
   export AWS_PROFILE=ii-dev
3: ssoアカウントの場合
　 aws sso login --profile ii-dev

=========== コード実行 ===========
1: ターミナルで以下コマンド実行（ii-devはprofile名です、適宜変更してください）
   python check.py --profile ii-dev
2: output.txtに結果が表示されます
　 結果を一旦新しいスプレッドシートにコピーして利用するのを推奨します
   最大CPU使用率は過去30日の5分平均の最大値を取得しています

=========== 修正予定 ===========
EBSの複数表示
DocDB、ElastiCacheの単一インスタンスの表示