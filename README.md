# 環境構築
* レポジトリダウンロード。git clone https://github.com/YuskeK/template-eda.git my_project
  * プロジェクトテンプレートで使用してもいいが、手元で使うぐらいがメインなのでフォルダ名を変更するぐらいで基本OK
* このプロジェクトではuvを使用. `uv sync`でパッケージインストール可能
* pyprojectのnameを変更する

# notebookのhtmlへの変換
* plotlyを使うなら以下も追加
  ```python
  import plotly.io as pio
  # HTML出力時にJavaScriptをフルで埋め込む設定
  pio.renderers.default = "plotly_mimetype+notebook"
  ```
* `jupyter nbconvert --to html --execute --template classic --embed-images eda-kpi.ipynb`
* quartoを使用してドキュメントをレンダリングする場合
  * レンダリング.内部でpythonを使って描画とかをするのでuv runで実行する
    ```bash
    uv run quarto render my_project.qmd
    uv run quarto render temp2.qmd --output-dir "./report"
    ```

# コミットメッセージ 規約
* 詳細は [docs/COMMIT_CONVENTION.md](docs/COMMIT_CONVENTION.md) を参照してください。

# 実装 規約
* コーディングを実施する際は、以下のルールを守ること。
  * 明確にわかる処理についてコメントを入れないこと。複雑な処理、なぜやっているのか分からなくなるような処理に対してコメントを入れること
  * 共通化できる処理はsrc/配下で関数化・クラス化して管理すること。
  * ただし、実装時はクラスなどを使用しすぎず適度にシンプルさを保つこと。