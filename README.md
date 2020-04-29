# adguard_settings_5chスレ版_超初心者向けとりあえずAdguard入れたけどなにすればいい？これインポートするんだ

## 最初に
　すでになにか設定している場合には、**試す前に設定バックアップ**をしましょう。

　問題や足りないのがあれば5chスレで教えて。

## これは？
**とりあえずAdguard入れたけどなにすればいい？**  
**これインポートするんだ**

　[【広告除去】AdGuard Part36【280blocker】 ](https://egg.5ch.net/test/read.cgi/android/1585413705/)の[87](https://egg.5ch.net/test/read.cgi/android/1585413705/87)氏の提言を参考に、簡単にAdguardのセットアップをするための超初心者向けインポート用設定ファイル。
<details>
<summary>87氏の提言</summary>

> もう面倒だから最新版にして、280とDNSオン(280ドメイン)だけで使ってる  
> 何時までも旧バージョンに拘っても新機能や性能改善などでいつかはバージョンアップすることになるから
</details>

　これは提言のほかに`||アフィカスブログドメイン^`と`||sch.line.me^`を追加し、拡張機能を無効化したもの。  
　最低限のセットアップがこれをインポートするだけで簡単にほとんど終わります。
　このインポート用設定ファイルが対応するのは[3.3.3 Release(v3.3.231)](https://github.com/AdguardTeam/AdguardForAndroid/releases/download/v3.3.231/adguard-3.3.3-release.apk)(APK)以降です。
<details>
<summary>用語解説</summary>

- `||アフィカスブログドメイン^`  
	　5chスレに[Adguardアフィリエイトプログラム](https://aff.adguard.com/en/welcome.html)リンクやブログリンクを貼る荒らしのブログ。  
	　ブログドメインは`adsoku[.]blogspot[.]com`。
- `||sch.line.me^`  
	　[LINEアプリ](https://play.google.com/store/apps/details?id=jp.naver.line.android)のトークリストにある広告ドメイン。  
	　有料ならコンテンツブロックのUser rulesに`||sch.line.me^$app=jp.naver.line.android`を追加してもOK。  
	　DNSユーザーフィルタに追加しているのは慣習。（無料向け）
- 最低限のセットアップ  
	　異論多数。  
	　内製フィルタを使うべきだ、外部フィルタを使うべきだ、HTTPSは、DNSは、と異論多数。  
	　それは初心者や初心者を脱する人向けと割り切り、**超初心者**が必要最低限のセットアップを素早く簡単にできることを目的にしてます。
</details>

## 使い方

### ダウンロードの仕方
**[直リンク](https://github.com/ag-nanashi/adguard_settings-json-For-super-beginners-at-5ch/raw/master/adguard_settings_3.3.3%28v3.3.231%29%E4%BB%A5%E9%99%8D%E7%94%A8_5ch%E3%82%B9%E3%83%AC%E7%89%88_%E8%B6%85%E5%88%9D%E5%BF%83%E8%80%85%E5%90%91%E3%81%91%E3%81%A8%E3%82%8A%E3%81%82%E3%81%88%E3%81%9AAdguard%E5%85%A5%E3%82%8C%E3%81%9F%E3%81%91%E3%81%A9%E3%81%AA%E3%81%AB%E3%81%99%E3%82%8C%E3%81%B0%E3%81%84%E3%81%84%EF%BC%9F%E3%81%93%E3%82%8C%E3%82%A4%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%88%E3%81%99%E3%82%8B%E3%82%93%E3%81%A0.json)**  
**[zip直リンク](https://github.com/ag-nanashi/adguard_settings-json-For-super-beginners-at-5ch/blob/master/adguard_settings_3.3.3%28v3.3.231%29%E4%BB%A5%E9%99%8D%E7%94%A8_5ch%E3%82%B9%E3%83%AC%E7%89%88_%E8%B6%85%E5%88%9D%E5%BF%83%E8%80%85%E5%90%91%E3%81%91%E3%81%A8%E3%82%8A%E3%81%82%E3%81%88%E3%81%9AAdguard%E5%85%A5%E3%82%8C%E3%81%9F%E3%81%91%E3%81%A9%E3%81%AA%E3%81%AB%E3%81%99%E3%82%8C%E3%81%B0%E3%81%84%E3%81%84%EF%BC%9F%E3%81%93%E3%82%8C%E3%82%A4%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%88%E3%81%99%E3%82%8B%E3%82%93%E3%81%A0.zip?raw=true)**
- *ブラウザにリンク先をダウンロードがある場合*は上のリンクを長タップなどする
- *ダウンローダーアプリの場合*は上のリンクを共有でダウンローダーアプリに渡す
- zip形式の取り扱いについては[検索結果](https://www.google.co.jp/search?tbs=qdr:m6&q=%22android%22%20AND%20%22zip%22%20AND%20%22%E8%A7%A3%E5%87%8D%22%20AND%20%22%E6%96%B9%E6%B3%95%22%20OR%20%22%E3%82%84%E3%82%8A%E6%96%B9%22%20OR%20%22%E3%81%8A%E3%81%99%E3%81%99%E3%82%81%22)からご自身で判断してください

### インポートの仕方
1. Adguardを起動
1. 左上の`≡`をタップ
1. `設定`をタップ
1. `一般設定`をタップ
1. `設定をインポート`をタップ
1. ダウンロードしたファイルをタップして、インポート

### インポートの後にすること
- 有料
	1. ライセンス状態の復帰
	1. HTTPSをどうするか
- 無料
	1. コンテンツブロックのUser rulesに[280blocker_adblock.txt](https://280blocker.net/files/280blocker_domain_ag.txt)インポート
	1. HTTPSをどうするか

<details>
<summary>HTTPSについて</summary>

　HTTPSについては、[HTTPSフィルタリングについて](https://wikiwiki.jp/nanj-adguard/HTTPS%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)を読んでご自身で判断してください。  
　[HTTPSフィルタリングについて](https://wikiwiki.jp/nanj-adguard/HTTPS%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%83%AA%E3%83%B3%E3%82%B0%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)が正しいか誤りかもご自身で判断してください。  
　なお`HTTPSフィルタリング`を有効にしない場合は広告が漏れます。  
　また使用する[280blocker](https://280blocker.net/)のフィルタは`HTTPSフィルタリング`の有効が前提です。
</details>

### 定期的にしなくてはいけないこと

- 有料
	1. なし
- 無料
	1. [280blocker_adblock.txt](https://280blocker.net/files/280blocker_domain_ag.txt)をときどき手動更新

## その他

<details>
<summary>知識を得た将来に自分で選択すべきこと</summary>

### 知識を得た将来に自分で選択すべきこと
- 有料
	1. フィルタの選択
	1. ステルスを使うかどうか
	1. 拡張機能を使うかどうか
- 無料
	1. 有料にするかどうか
</details>

<details>
<summary>デフォルトからの変更・更新点</summary>

### デフォルトからの変更・更新点

#### 変更したもの
- コンテンツ
	1. 内製フィルタ（Adguard公式が用意したフィルタ）の無効化
- DNS
	1. 有効化
	1. `AdGuard 簡易ドメインフィルタ`の無効化
- その他
	1. 拡張機能の無効化

#### 追加したもの
- コンテンツ: カスタムフィルタ
	1. `https://280blocker.net/files/280blocker_adblock.txt`
- コンテンツ: ユーザールール
	1. インポート履歴に`https://280blocker.net/files/280blocker_adblock.txt`
- DNS
	1. `||アフィカスブログドメイン^`
	1. `||sch.line.me^`
	1. `https://280blocker.net/files/280blocker_domain_ag.txt`

#### 追加したもの（デフォルト無効）
　著名なフィルタを登録しています。  
　スレで紹介された中で継続してメンテナンスされているか現在も有効な中から独断と偏見で選び登録しています。  
　これらは登録していますが**有効化していません**。  
　のちのちフィルタを追加する手間を省くために登録だけしてあります。

- コンテンツ
	1. [たまごフィルタ](https://raw.githubusercontent.com/eEIi0A5L/adblock_filter/master/tamago_filter.txt)
	1. [豆腐フィルタ](https://raw.githubusercontent.com/tofukko/filter/master/Adblock_Plus_list.txt)
	1. [もちフィルタ](https://raw.githubusercontent.com/eEIi0A5L/adblock_filter/master/mochi_filter.txt)
	1. [なんJ改修フィルター](https://raw.githubusercontent.com/nanj-adguard2/nanj-kaishuu-filter/master/nanj-kaishuu-filter.txt)  
	信頼するフィルタ: **有効**
	1. [なんJ拡張フィルター：一般ルール](https://raw.githubusercontent.com/nanj-adguard2/nanj-kakuchou-filter/master/supplement-rules.txt)  
	信頼するフィルタ: **有効**
	1. [なんJ拡張フィルター：Paranoidルール](https://raw.githubusercontent.com/nanj-adguard2/nanj-kakuchou-filter/master/paranoid-rules.txt)  
	信頼するフィルタ: **有効**
	1. [chmate0.8.10.62ブロックルール<有料専用版>](https://pastebin.com/raw/RbfDWJMx)
	1. [AdGuard Japanese Mobile Site Filter FA-FA(仮)](https://raw.githubusercontent.com/sa-ki13/jmsf/master/japanese_mobile_site_filter.txt)
	1. [対AdGuard Affiliate Program2](https://pastebin.com/raw/LBCYrHdJ)  
	信頼するフィルタ: **有効**
- DNS
	1. [ABP版: 280blocker for japanese mobile site](https://280blocker.net/files/280blocker_adblock.txt)
	1. [hosts2ch - Japanese mobile ad servers only](https://sites.google.com/site/hosts2ch/ja)
	1. [なんJ改修DNSフィルター](https://raw.githubusercontent.com/nanj-adguard2/nanj-kaishuu-filter/master/nanj-kaishuu-dns-filter.txt)
	1. [なんJ拡張フィルター：DNSルール](https://raw.githubusercontent.com/nanj-adguard2/nanj-kakuchou-filter/master/DNS-rules.txt)
	1. [chmate0.8.10.62ブロックルール<有料専用版>](https://pastebin.com/raw/RbfDWJMx)
	1. [chmate0.8.10.62ブロックルール<無料専用版>](https://pastebin.com/raw/vHRJk5xD)
</details>

### 素朴な疑問

<details>
<summary>なぜ内製フィルタを使わない？</summary>

#### なぜ内製フィルタを使わない？
　**超初心者**には英語が前提になるAdguardサポートとのコミュニケーションはむずかしいです。  
　[280](https://280blocker.net/)氏なら日本語でやりとりできます。

　あと一番はスレの昔からの慣習。
</details>

<details>
<summary>広告が出たら？</summary>

#### 広告が出たら？
　`HTTPSフィルタリング`を有効にしない場合は広告が漏れます。  
　また使用する[280blocker](https://280blocker.net/)のフィルタは`HTTPSフィルタリング`の有効が前提です。

　`HTTPSフィルタリング`を有効にしているのに広告が出たら、[消えない広告・連絡について](https://280blocker.net/checkblock/)を開き、「広告ブロックアプリの動作チェック」を確認してから、「広告の報告」を経由して[280](https://280blocker.net/)氏に報告してください。  
　もしくはスレで相談しましょう。
</details>


