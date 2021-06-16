# Gitメモ

## タグ

リモートリポジトリのタグ(TAGNAME)を削除する。

```bash
git push --delete origin TAGNAME
```

## restore

指定されたファイルなどを「戻す」ことができる。

```
git restore <コミットID> <ファイルパス>
```

特定のコミット時点に戻すことも可能。

[これからは git restore を使ってみようかな \- Mitsuyuki\.Shiiba](https://bufferings.hatenablog.com/entry/2020/05/01/013451)に書いてある図がわかりやすい。
