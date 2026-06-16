[README.md](https://github.com/user-attachments/files/29004757/README.md)
# ApkExtractor# APK Extractor

インストール済みのアプリを APK ファイルとして抽出する Android ユーティリティアプリです。

## 機能

- インストール済み全アプリの一覧表示（システムアプリ・ユーザーアプリ）
- アプリ名・パッケージ名でのリアルタイム検索
- 保存先フォルダを自由に選択（端末内蔵ストレージ / SD カード）
- 複数アプリを選択して一括抽出
- 抽出進捗をリアルタイム表示
- 保存先フォルダはアプリ再起動後も維持
- ファイル名は `{アプリ名}_{バージョン}.apk` 形式

## スクリーンショット

| アプリ一覧 | 保存先フォルダ選択 | 抽出中 |
|:---:|:---:|:---:|
| ![Main](docs/screenshot_main.svg) | ![Folder](docs/screenshot_folder.svg) | ![Extracting](docs/screenshot_extracting.svg) |

## 動作環境

- Android 8.0（API 26）以上
- ビルド環境: JDK 17、Android SDK 36

## 使い方

1. アプリを起動するとインストール済みアプリが一覧表示されます
2. 「保存先フォルダを選択」ボタンで APK の保存先を変更できます（省略時はアプリ内部ストレージ）
3. 検索またはスクロールで目的のアプリを探します
4. 抽出したいアプリにチェックを入れます
5. 「Extract (N)」ボタンをタップして抽出を開始します
6. 完了後、選択したフォルダに APK ファイルが保存されます

抽出した `.apk` ファイルは以下の用途に使えます:
- ファイルマネージャーからタップしてインストール
- 他の端末に転送してインストール
- `adb install ファイル名.apk` でインストール

## ビルド方法

```sh
# デバッグビルド
./gradlew assembleDebug

# リリースビルド（署名キーが必要）
./gradlew assembleRelease
```

## 依存ライブラリ

| ライブラリ | バージョン |
|-----------|-----------|
| Material Components | 1.11.0 |
| AndroidX Core KTX | 1.12.0 |
| AndroidX AppCompat | 1.6.1 |
| RecyclerView | 1.3.2 |
| CardView | 1.0.0 |
| DocumentFile | 1.0.1 |
| Kotlin Coroutines | (バンドル) |

## ライセンス

個人利用・教育目的で自由にお使いいただけます。
