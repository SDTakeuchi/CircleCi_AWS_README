# CircleCI ✖︎ AWSでCI/CDを体験しよう！！

## はじめに
### CI/CDとは

CI/CDとは高度な継続的自動化と継続的監視をアプリケーション開発に取り組むこと、また、そのプロセスのこと

![image](https://user-images.githubusercontent.com/66664167/92073666-39264f00-edef-11ea-8e05-c9db7127b3e9.png)

<br>
<br>

### - 継続的インテグレーション　-

>継続的インテグレーションは、コードを共有リポジトリの master ブランチに常時頻繁に統合することを奨励する開発手法です。それぞれの機能を個別にビルドして、開発サイクルの最後に統合するのではなく、各開発者のコードが 1 日に何度も共有リポジトリに統合されます。
>すべての開発者が共有メインラインに毎日コミットします。コミットされるたびに、自動化されたビルドとテストがトリガーされます。ビルドやテストが失敗しても、数分以内にすばやく修復できます。
>チームの生産性、効率、満足度を向上させます。 問題をすばやく検出して解決できます。 より高品質で安定したプロダクトをリリースできます。
<br>
※　CircleCi公式ドキュメントより：https://circleci.com/docs/ja/2.0/about-circleci/#section=welcome
<br>

![image](https://user-images.githubusercontent.com/66664167/92101045-83232b00-ee17-11ea-89d9-38ee6caee2df.png)

<br>
※　技術評論社より：https://gihyo.jp/book/pickup/2015/0045
<br>

### - 継続的デリバリー -
>検証されたコードのリポジトリへのリリースを自動化します。継続的デリバリーの目標は、本番環境にデプロイできるコードベースを常に保持しておくことです。
継続的デリバリーでは、コード変更のマージから本番環境対応のビルドのデリバリーまで、すべてのステージでテストの自動化とコードリリースの自動化が実施されます。このプロセスの終了時には、運用チームはアプリケーションを本番環境にすばやく簡単にデプロイできます。
<br>

### - 継続的デプロイメント -
>成熟した CI/CD パイプラインの最終ステージは、継続的デプロイメントです。本番環境対応のビルドをコードリポジトリへ自動的にリリースする継続的デリバリーの延長として、継続的デプロイメントはアプリケーションを本番環境に自動的にリリースします。本番環境に移す前のパイプラインのステージでは手動でのチェックはないので、継続的デプロイメントは主に、入念に設計されたテスト自動化を活用します。
<br>
<br>

## なぜCI/CDなのか？
#### ・自動化テストの重要性の高まり<br>
これだけソフトウェアが普及していくと、品質に対する要求も高くなり、今まで手動でテストしていた分野でも積極的に自動化テストを取り入れるようになってきます。なぜならCI/CDを使うと、コードの変更が発生するたびに自動でテストが行われるので、テストの実行忘れや、環境依存のテストを失くすことでの品質を向上させることができるからです。

#### ・アジャイル開発のプラクティスの浸透と進化<br>
アジャイル開発で重要なことはスピードです。より小さな粒度の変更をいかに早くテスト／リリースしてフィードバックを得るかがアジャイル開発の成功の鍵となりますが、CI/CDを使うことでこれらを実現することができます。
<br>
<br>

## CI/CDツール選定
### Jenkins
![image](https://user-images.githubusercontent.com/66664167/92107197-5a536380-ee20-11ea-95b5-6488c0ecb79f.png)
#### - メリット - <br>
#NAME?
#NAME?
#NAME?

#### - デメリット - <br>
#NAME?
#NAME?
#NAME?

### TravisCI
![image](https://user-images.githubusercontent.com/66664167/92107394-a9999400-ee20-11ea-80af-30f183fb4802.png)
#### - メリット - <br>
#NAME?
#NAME?
#NAME?

#### - デメリット - <br>
#NAME?
- $129がかかるため、CIをはじめて導入する際には提案しにくい
#NAME?

### CircleCI
![image](https://user-images.githubusercontent.com/66664167/92107539-ecf40280-ee20-11ea-8651-7261697f7995.png)
#### - メリット - <br>
#NAME?
#NAME?
#NAME?
#NAME?
#NAME?

#### - デメリット - <br>
#NAME?
#NAME?
<br>
<br>

## ★　今日やること　★

### 1.目的
### 2.今日のゴール
### 3.環境・言語
### 4.事前準備
#NAME?
- AWS EC2インスタンの起動、Elastic IPの設定　[設定方法はこちら](https://github.com/miracleave-ltd/aws_ec2)
#NAME?
#NAME?
#NAME?

## .やってみよう！

### 1. リポジトリを作成
#### 1-1 GitHubにアクセスする
[こちらから該当ファイルを取得する](https://github.com/miracleave-ltd/meet-up_CI-CD)

#### 1-2 ZIPファイルをダウンロードする
![image](https://user-images.githubusercontent.com/66664167/92227895-f3967e80-eee1-11ea-9584-617df0e14f53.png)

#### 1-3 ローカルにディレクトリを作り、ダウンロードしたファイルを格納する
ターミナルを使用します。

> // ディレクトリ作成(任意の場所を指定して作成してください）<br>
> $ mkdir [ファイルの格納場所のパス]/[ディレクトリ名]<br>
> 例：$ mkdir mkdir ~/projects/myapp

#### 1-4 自分のGitHubにリポジトリを作成する
GitHubにログインして「New」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92230424-0f038880-eee6-11ea-967b-de06bb69fd20.png)

「Repository name」を入力、「Public」にチェック（初期値）、「Create repository」ボタン押下し作成する
（今回はmy-favarite-bookで設定)
![image](https://user-images.githubusercontent.com/66664167/92229246-20e42c00-eee4-11ea-8da7-aa408c91ee17.png)

リポジトリ作成後画面
![image](https://user-images.githubusercontent.com/66664167/92230877-c6989a80-eee6-11ea-942a-76feac5c08ad.png)


#### 1-5 ローカルの該当ソースをリポジトリに反映する
> $ git init <br>
> $ git add .<br>
> $ git commit -m "init" <br>
> $ git branch -M master <br>
> $ git remote add origin https://github.com/[ユーザー名]/[リポジトリ名].git <br>
> $ git push -u origin master <br>

リポジトリ反映後画面
![image](https://user-images.githubusercontent.com/66664167/92231621-07dd7a00-eee8-11ea-826a-235b83254d4b.png)


### 2. 初期設定
Laravelのライブラリパッケージ等をdockerコンテナ内にインストールする

#### 2-1 コンテナを立ち上げる
> $ docker-compose up -d

#### 2-2 dockerコンテナに入る
> $ docker-compose exec app bash

#### 2-3 インストールする
> $ cd my-laravel-app && composer install && cp ../docker/laravel/.env .env && chmod 777 -R storage/ && php artisan key:generate && php artisan config:cache && php artisan migrate 
<br>

> // コンテナを抜ける <br> $ exit 

#### 2-4 再起動する 
> $ docker-compose down && docker-compose up


#### 2-5 ローカル上でアプリの起動を確認する
http://localhost:8989 にアクセスする

### 3.EC2の設定

--------------上野くん----------------


### 4 CircleCIの設定
#### 4-1 ログインする
https://circleci.com/ja/vcs-authorize/

![image](https://user-images.githubusercontent.com/66664167/92234453-095d7100-eeed-11ea-8730-beb61574538a.png)


#### 4-2 該当プロジェクトの設定をする
##### 4-2-1 該当プロジェクトの「Set Up Project」を押下する
![image](https://user-images.githubusercontent.com/66664167/92300453-c6a3a380-ef95-11ea-8aee-ab2a4078691c.png)

##### 4-2-2 「Use Existing Config」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300489-2ac66780-ef96-11ea-922c-d56902bea456.png)

##### 4-2-3 「Start Building」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300523-7aa52e80-ef96-11ea-8856-8511d7febf14.png)

#### 4-3 EC2インスタンスと関連付ける
テストが開始される（各種設定前なのでFAILDになるが問題ありません）
##### 4-3-1 「Project Setting」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300761-7417b680-ef98-11ea-9a75-a0ae99371953.png)

##### 4-3-2 メニューの「SSH Keys」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92300833-16379e80-ef99-11ea-87de-99bc615f8c53.png)

##### 4-3-3 ターミナルを開き、EC2インスタンスにログインして、SSH Keyをコピーする

> // EC2にログイン<br>
> $ ssh -i ~/.ssh/[pem key名] [ユーザー名]@[IP]<br>

> // SSH Keyが表示される<br>
> $ cat ~/.ssh/id_rsa

コピーする
![image](https://user-images.githubusercontent.com/66664167/92301975-2d7b8980-efa3-11ea-9ab9-461ff58fa09b.png)


##### 4-3-4 ページ下部の「Add SSH Keys」ボタンを押下すし、IPアドレスとコピーしたKeyを入力する
![image](https://user-images.githubusercontent.com/66664167/92301125-d58d5480-ef9b-11ea-9f27-ee3ce9b92fdc.png)
![image](https://user-images.githubusercontent.com/66664167/92302429-23f42080-efa7-11ea-8730-1d28548e33ef.png)


#### 4-4 環境変数を設定する
##### 4-4-1 メニューの「Organization Settings」ボタンを押下する
![image](https://user-images.githubusercontent.com/66664167/92302693-0d4ec900-efa9-11ea-9f7f-e80315837035.png)

##### 4-4-2 メニューの「Contexts」を選択（初期画面）し、「Create Context」を押下する
![image](https://user-images.githubusercontent.com/66664167/92478693-7f2f4880-f21d-11ea-8415-d0338347fc9f.png)

##### 4-4-3 「Context Name」に任意の名前を入力し、「Create Context」を押下する（例：meet-up）
![image](https://user-images.githubusercontent.com/66664167/92479021-f95fcd00-f21d-11ea-9058-81509b3171a5.png)

##### 4-4-4 前画面に戻るので、入力した名前があるか確認し、該当のNameを押下する
![image](https://user-images.githubusercontent.com/66664167/92479460-87d44e80-f21e-11ea-947a-5a8ed7b8e1f9.png)

##### 4-4-5 「Add Environment Variables」を押下する
![image](https://user-images.githubusercontent.com/66664167/92479794-f6191100-f21e-11ea-8d4a-ade01ec2fd12.png)

##### 4-4-6 「Environment Variable Name」と「Value」にそれぞれ下記の通り入力し、 「Add Environment Variables」を押下する

① Environment Variable Name: USER_NAME
　 Value: EC2インスタンスのユーザー名（例：ec2-user）
  
② Environment Variable Name: HOST_NAME
　 Value: EC2インスタンスのIPアドレス

![image](https://user-images.githubusercontent.com/66664167/92480545-01b90780-f220-11ea-9379-feb90dc1c7c3.png)

###### 入力後の画面にてそれぞれName,Valueが入っていることを確認する
![image](https://user-images.githubusercontent.com/66664167/92481230-0205d280-f221-11ea-8325-9c25d2ba924f.png)



















CI/CD パイプラインのさまざまなテストおよびリリースステージに合わせて自動化されたテストを作成する必要があるため、まとまった事前の投資も必要です。
