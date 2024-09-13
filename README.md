# Mirror4Avatar

## 概要

Fake mirrors for avatars アバター用ミラーっぽいやつ

ミラーっぽい挙動の実装はこちらを参考にしました→[Unityで鏡を実装する方法](https://qiita.com/nkjzm/items/ccba41a6e7e5211aae95)

常にアバターの方を向くのであまりワールド据え置きミラーっぽくはないかも

## インストール

### VCCによる方法

1. https://vpm.narazaka.net/ から「Add to VCC」ボタンを押してリポジトリをVCCにインストールします。
2. VCCでSettings→Packages→Installed Repositoriesの一覧中で「Narazaka VPM Listing」にチェックが付いていることを確認します。
3. アバタープロジェクトの「Manage Project」から「Mirror4Avatar」をインストールします。

## 使い方

Packages/Mirror4Avatarの中にある好きなプレハブをアバターに突っ込む。

一枚鏡（MirrorCamera）と四面鏡(MirrorCameras)、ワールド固定(WorldPlacer)あるなしがあります。

## License

[Zlib License](LICENSE.txt)
