# 環境構築
* レポジトリダウンロード。git clone https://github.com/YuskeK/template-eda.git my_project
  * プロジェクトテンプレートで使用してもいいが、手元で使うぐらいがメインなのでフォルダ名を変更するぐらいで基本OK
  * プロジェクトテンプレートとして使用する場合は、リポジトリ作成画面で選択する
* このプロジェクトではuvを使用. `uv sync`でパッケージインストール可能
* pyprojectのnameを変更する

# notebookのhtmlへの変換
* 詳細は [docs/ipynb2html.md](docs/ipynb2html.md) を参照してください。

# Quartoの環境構築
* 詳細は [docs/setup-quarto.md](docs/setup-quarto.md) を参照してください。

# コミットメッセージ 規約
* 詳細は [docs/commit-convention.md](docs/commit-convention.md) を参照してください。

# 実装 規約
* コーディングを実施する際は、以下のルールを守ること。
  * 明確にわかる処理についてコメントを入れないこと。複雑な処理、なぜやっているのか分からなくなるような処理に対してコメントを入れること
  * 共通化できる処理はsrc/配下で関数化・クラス化して管理すること。
  * ただし、実装時はクラスなどを使用しすぎず適度にシンプルさを保つこと。  