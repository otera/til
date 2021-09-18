# ブラウザメモ

# User-Agent文字列

ユーザーエージェント（UA）文字列はWebブラウザーの種類やバージョン、プラットフォーム（OS）などを特定するために使うことが可能。  
2021年9月18日現在 `navigator.userAgent` を実行すると `'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/93.0.4577.82 Safari/537.36'` が返ってくる。

Google ChromeではUser-Agent文字列を非推奨として段階的に[UserAgent文字列の更新を停止する計画](https://forest.watch.impress.co.jp/docs/serial/yajiuma/1229968.html)がある。  
新たに`User Agent Client Hints`というものが提供されるので、今後はこちらを利用する。

参考リンク

- [【重要】Chromeでユーザーエージェントが廃止される【対処方法も解説】](https://it-web-life.com/chrome_user_agent_abolished/)
- [ChromeでUserAgentが凍結される日（User Agent Client Hintsの使い方） \- Qiita](https://qiita.com/paddy-oti/items/fae9ecca9facc9797035)
