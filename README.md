# MakeAtomCraftData

## タイトル
MakeAtomCraftData（CRI Atom Craftのデータ自動生成ツール）

## 概要
CRI Atom Craft向けのワークユニット（ACB）や全体設定（ACF）を、Unity5上のC#スクリプトで自動生成します。Assets/Materials配下のwavファイルを元にキューを作成し、Assetsフォルダ以下に指定名のワークユニットフォルダを生成します。

## 構成
- MakeAtomCraftData.cs：ワークユニット（ACB）生成用のEditorスクリプト
- MakeAtomCraftACF.cs：全体設定（ACF）生成用のEditorスクリプト
- README.md：導入・使い方・注意事項

#セットアップ
* Assets下にEditorフォルダを作成します。
* EditorフォルダにMakeAtomCraftData.cs、MakeAtomCraftACF.csをコピーします。

## 使い方
### 1. ワークユニットファイル（ACB）の生成
* Assets下にMaterialsフォルダを用意します。
* 使いたい波形（wav）をMaterialsに登録します。
* メニュー「CRI>My>Open MakeAtomCraft...」を選択します。
* キューシート名を設定して「Make Atom Craft Data」ボタンを押します。

### 2. 全体設定（ACF）の生成
* メニュー「CRI>My>Open MakeAtomACF...」を選択します。
* ACF名、カテゴリを設定して「Make Atom ACF Data」ボタンを押します。

### 3. AtomCraftへの読み込み
できあがったatmcglobalsやwrokunitフォルダを、新規作成したAtomCraftのファイルへ上書きします。

## 主な機能
- Assets/Materials配下のwavからキューを自動生成
- ACB（ワークユニット）フォルダを指定名で自動作成
- ACF（全体設定）データの自動生成

動画→https://www.youtube.com/watch?v=vCJa73xqK6I
（仕様が変わったのでワークユニットに登録するところのみ参考に）

# 注意
- Assetsフォルダにキューシート名のフォルダが既にある時はあらかじめ削除してから開始してください。
- グループ／カテゴリの設定は全体設定側で正しく行った状態で読み込まないと読み込み時リンクエラーが発生します。この場合はグループ／カテゴリを正しく作成しなおしてください。
- CRI Atom CraftはVer.2.14.00、Unityは5.1.0f3で動作確認しています。
