# Nature Remo BLE Macro Collection

このリポジトリは、Nature Remo向けのBLE（Bluetooth Low Energy）マクロファイルを管理するプロジェクトです。

## 概要

Nature RemoのBLEマクロ機能を使用して、BLEデバイスを制御するためのXMLファイルを提供しています。

詳細については以下のドキュメントをご参照ください：
https://engineering.nature.global/entry/ble-macro-control-beta

## 利用可能なマクロ

### デバイス制御マクロ

- `turn_on_if_off.xml` - デバイスがオフ状態の場合のみオンにする
- `turn_off_if_on.xml` - デバイスがオン状態の場合のみオフにする

## マクロファイルの構造

各マクロファイルは以下の要素で構成されています：

- **Service UUID**: `932c32bd-0000-47a2-835a-a8d455b859dd`
- **Characteristic UUID**: `932c32bd-0002-47a2-835a-a8d455b859dd`
- **状態確認**: 現在のデバイス状態を読み取り
- **アクション実行**: 適切な値（0x00/0x01）を書き込み
- **通知確認**: 操作完了の通知を待機

## 使用方法

1. Android端末にnRF Connectアプリをインストール
2. Nature RemoアプリでBLEデバイスを登録
3. このリポジトリのXMLファイルURLを使用してマクロボタンを追加
4. Nature Remoアプリからマクロを実行

## ファイル管理ポリシー

**重要**: このリポジトリでは以下のポリシーに従います：

- **既存ファイルの削除・修正は行いません**
- 変更が必要な場合は、以下の方法で対応します：
  - 新しいファイル名で作成（例：`turn_on_if_off_v2.xml`）
  - バージョン管理用ディレクトリの作成（例：`v2/`ディレクトリ）
  - 機能別ディレクトリの作成

このポリシーにより、既存のマクロを使用しているユーザーへの影響を最小限に抑え、後方互換性を保証します。

## 参考資料

- [BLE macro control beta - Nature Engineering Blog](https://engineering.nature.global/entry/ble-macro-control-beta)
- [BLE Macro Examples Repository](https://github.com/tomoyuki-nakabayashi/blemacro_examples)
