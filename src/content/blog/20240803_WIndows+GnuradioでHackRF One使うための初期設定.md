---
title: "WIndows+GnuradioでHackRF One使うための初期設定"
description: "Windows環境でradiocondaとZadigを使い、GnuradioからHackRF Oneを使うための初期設定手順。"
pubDate: 2024-08-03
---

## radiocondaのインストール
こちらに従ってインストール。
Gnuradioを動かすためのいろいろがまとめてインストールできます。
今回は楽をしたいのでこちらを使います。
https://github.com/ryanvolz/radioconda#additional-installation-for-device-support
自身のOSに合わせてインストーラをダウンロードして実行します。
このとき、既にAnacondaがインストールされていてもそのままで問題ないそうですが、私の環境だとかなり古いAnacondaが導入されていたので、念の為事前にアンインストールしておきました。
![](./20240803_WIndows+GnuradioでHackRF%20One使うための初期設定/download.png)

## Zadigを使ってHackRF One のドライバーをインストール
こちらに従ってドライバーインストール。
https://github.com/pbatard/libwdi/wiki/Zadig
まず、Zadigをダウンロードし、実行する。
HackRF OneをPCにUSB接続し、ZadigのドロップメニューからHackRF Oneを選択する。
ドロップメニューになにも表示されない場合は、Options>List All Devices にチェックを入れる。
![](./20240803_WIndows+GnuradioでHackRF%20One使うための初期設定/zadig.png)
ドロップメニューからHackRF Oneを選択したら、Install WCID Driverをクリックする。

## 起動してみる
WindowsのスタートメニューにGnuradioが現れたので、こちらをクリックします。
![](./20240803_WIndows+GnuradioでHackRF%20One使うための初期設定/gnuradio01.png)
すると、ちゃんと起動しました。
画面右側にはHackRF Oneで入出力を行うための、OsmoSDRという機能ブロックが追加されていることが確認できます。
![](./20240803_WIndows+GnuradioでHackRF%20One使うための初期設定/gnuradio02.avif)
