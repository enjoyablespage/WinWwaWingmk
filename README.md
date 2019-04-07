WinWwaWingmk
===
WWA作成ツールのWWA Wingカスタマイズ版です。 まだ本家から大きな動きはないです。 
本家のzipファイルの中身をベースにしています。

本家のソースは [キャラバンサークルのページ](http://www.wwajp.com/making.html) からダウンロードできます。

## 始め方
このプロジェクトは、 Visual Studio 2019 に対応しています。

### MFC の追加
まず最初に、MFCライブラリを追加してください。

1. 追加画面まで移動します
    - Visual Studio を初めてインストールする場合は既にその画面になっていると思います。
    - 既に Visual Studio がインストールされている場合は、 Visual Studio Installer で対象のVisual Studioから **変更** を選ぶと追加画面が表示されます。
2. **C++ によるデスクトップ開発** を選択します。
3. 上部のタブから **個別のコンポーネント** を選択し、その中から **(バージョン) ビルドツール用 C++ MFC (x86 および x64)** を選びます。
    - 💡 使用するバージョンはできるだけ最新のバージョンをご利用ください。2019年4月7日現在、最新のバージョンは **v142** となります。
4. あとは インストール または 変更 でインストールします。

### 実行方法
Visual Studio を起動し、 ソリューションファイル `WinWwamk.sln` を開くと、当ツールの開発画面が表示されます。
あとは、 `WinWwamk.cpp` を開いて、上部の三角ボタンから実行することができます。

## 配布ファイルの内容について
WWAマップ作成ツールのソースコードにある説明を抜粋しています。

### ソースファイル
- `WinWwamk.cpp` 作成ツールのメインプログラムのソース
- `Script2.rc` リソースファイル
- `resource.h` リソースのファイルのヘッダ

上記の３つがプログラムの本体です。
リソースファイルには主に作成ツールで使われているウィンドウ群のレイアウトが定義されています。
ツールの改造は主に「WinWwamk.cpp」に変更を加えていく作業になると思います。
開発にはＣ＋＋言語の知識が必要になります。

### CDIB ライブラリ
- `CDIB.CPP` ビットマップ画像読み込み用のライブラリ
- `CDIB.HPP` 「CDIB.CPP」のヘッダ

この２つは開発の最初期にＧＩＦ画像が読み込めない環境に対応するために
使っていたBMP画像読み込み用のライブラリです。
「WinWwamk.cpp」などと共に作成ツールのコンパイルに必要です。
現在では遺物のため本体仕様からの切り離しが望ましいと思われます。

### プロジェクトファイル
- `WinWwamk.sln` Visual Studio のソリューションファイル
- `WinWwamk.vcxproj` コンパイル用のプロジェクトファイル

「Visual Studio Community」用のプロジェクトファイルです。
Communityをインストールしていれば、これを開いてビルドを選択することで、
そのまま「WinWwamk.exe」を作成できます。
これ自体は本来コンパイラごとに新規作成するものですので参考用です。

## ライセンス
LICENSE ファイルを参照。MITライセンスです。

(C)1996-2015 NAO
HomePage: http://www.wwajp.com
