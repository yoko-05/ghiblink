# [ghiblink（ジブリンク）]

## サービス概要
ジブリファン向けの情報収集、情報共有サービスです。

## 想定されるユーザー層
ジブリに関するイベント情報やグッズの入荷情報などを収集・共有をするために、
複数のサービスを横断して利用しているジブリファン

## サービスコンセプト
ジブリに関する情報は複数のサイトやサービス（例：Webサイト、X(旧Twitter)、Instagramなど）に点在しており、情報収集が大変だなと感じていました。  
実際に私が情報収集をする際、複数のWebサイトの横断や、XやInstagramを状況に応じて使い分けているのですが、どのサービスでどの情報が掲載されていたかわからなくなった経験がありました。  
また、ブラウザやアプリを切り替えるのが手間だなと感じたこともあります。
そこで、情報収集と情報共有がひとつのサービスで完結したら便利だなと思い、このサービスを考えました。  
また、このサービスを通じてファン同士での交流ができたら良いなと考えています。  

＜具体的な機能＞
* 本サービスのページ上に複数サイトやX、Instagramにポストされている情報を一元的に表示  
→　Twitter APIやInstagram Graph APIなどを使用することで、  
　　モバイルアプリを起動しなくても本サービス（Webアプリ）上で閲覧可能になり、  
　　情報を漏らすことなく取得できる。
* ポスト機能（投稿機能）で、ユーザー同士での情報共有が可能  
→　ポストに位置情報を含めることで閲覧者はGoogle Mapで簡単に場所を確認でき、  
　　投稿者は場所を明確に紹介できる。


## 実装を予定している機能
### MVP
* 会員登録
* ログイン
* ポスト（post）機能
* ポスト一覧
* ポスト詳細
* ポストへのいいね機能、ポスト保存機能
* スケジュール・イベント登録
* ジブリ公式サイト、SNSリンク集  
　◻︎ Webサイトからの情報取得：nokogiri(gem)を使用してスクレイピング  
　◻︎ X(Twitter)からの情報取得：Twitter API  
　◻︎ Instagramからの情報取得：Instagram Graph API  


### その後の機能
* 位置情報を含んだポストを投稿：Google Maps Platform
* 交流掲示板：ActionCable、WebSocket
* スケジュールのリマインド通知：Google Cloud Project、Google Calendar API


### 機能の実装方針予定
* Rails7系
* Ruby3系
* JavaScript
* Webサイトからの情報取得：nokogiri(gem)を使用してスクレイピング
* X(Twitter)からの情報取得：Twitter API
* Instagramからの情報取得：Instagram Graph API
* 位置情報：Google Maps Platform
* チャット機能：ActionCable、WebSocket
* スケジュール機能：Google Cloud Project、Google Calendar API
