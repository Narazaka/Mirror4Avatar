# Mirror4Avatar

## 概要

Fake mirrors for avatars アバター用ミラーっぽいやつ

ミラーっぽい挙動の実装は「[Unityで鏡を実装する方法](https://qiita.com/nkjzm/items/ccba41a6e7e5211aae95)」を参考にしました。「鏡面の描画」の項目までの実装です（「鏡の枠の設定」あたりからはシェーダー芸になりそうなので）。

挙動としては、常にアバターの方を向くので自分にしか正しく見えないです。あまりワールド据え置きミラーっぽくはないかも。

## インストール

### VCCによる方法

本パッケージをインストールする前に、Modular Avatarをインストールします。

1. https://vpm.narazaka.net/ から「Add to VCC」ボタンを押してリポジトリをVCCにインストールします。
2. VCCでSettings→Packages→Installed Repositoriesの一覧中で「Narazaka VPM Listing」にチェックが付いていることを確認します。
3. アバタープロジェクトの「Manage Project」から「Mirror4Avatar」をインストールします。

## 使い方

### アバターに配置する

1. Packages/Mirror4Avatarの中にある好きなプレハブをアバターに突っ込みます。

   一枚鏡（MirrorCamera）と四面鏡(MirrorCameras)、ワールド固定(WorldPlacer)あるなしがあります。

2. Prefabの中にあるViewPointオブジェクトをViewPointあたりに置いて下さい。四面鏡(MirrorCameras)版だと4つあるので全部一緒の場所に置いて下さい。

### 操作

ワールド固定は鏡の中心辺りのPBを掴んで置いて下さい。

鏡が自分にしか正しく見えないので、ワールド固定版付属のON/OFFは他人には表示されない設定になっています。

### 解像度

いったん各ミラー2048x2048です。デカいとか小さいとかの場合はRenderTextureの解像度を変えて下さい。

### 画角とか

正確にミラーっぽく見えるようにするには、カメラのFOVをHMDのFOVにあわせ、RenderTextureの縦横比で決まる画角をHMDのそれと合わせる必要があります。

だいたいのHMDのFOVは50～55らしいので、いったん52.5にしてあります。
https://docs.vrchat.com/docs/configuration-file#camera-and-screenshot-settings

## License

[Zlib License](LICENSE.txt)
