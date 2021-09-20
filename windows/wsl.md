# WSLメモ

WSLは`Windows Subsystem for Linux`の略で、Windows10上でLinuxを動作させる環境の事。

## WSL2とWSLの違い

> WSLは、Windows APIをLinux APIでラップしています。  
> WSLの下はWindowsのAPIなので「仮想」ではなく、いわば「Windowsのアプリケーション」なのです。  
>
> WSL2は完全な仮想環境です。  
> 仮想マシンをつくる、ハイパーバイザーの上でWindowsに全く依存しない形でLinuxカーネルごと起動します。  
> これまで仮想環境をつくるために導入していたVirtualBox、VMWareが要らなくなります。
>
> [WSL2とWSLの違いを解説します \- 情報技術の四方山話](https://blog.goo.ne.jp/takuminews/e/d89a8c8151fbc276333fe4ba2f6680f2)

## WSL2環境の構築

[WSL2を日本語化するときにやったこと](https://zenn.dev/ryuu/articles/wsl2-locale-jp)を参考に進める。

パッケージ情報のアップデートとパッケージのアップグレードを実行。

```
sudo apt update && sudo apt upgrade
```

日本語の言語パックのインストール

```
sudo apt install -y language-pack-ja
```

インストールの確認

```
$ locale -a
C
C.UTF-8
POSIX
en_US.utf8
ja_JP.utf8
```

日本語ロケールを設定

```
sudo update-locale LANG=ja_JP.UTF8
```

## WLS2の初期化

[WSL2のUbuntuを初期化する](https://zenn.dev/kawacdev/articles/3de7892fd13df3)を参考に実施する。