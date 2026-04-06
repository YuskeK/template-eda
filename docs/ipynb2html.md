# 標準的なhtml出力
* plotlyを使うなら以下も追加
  ```python
  import plotly.io as pio
  # HTML出力時にJavaScriptをフルで埋め込む設定
  pio.renderers.default = "plotly_mimetype+notebook"
  ```
* `jupyter nbconvert --to html --execute --template classic --embed-images eda-kpi.ipynb`

# quartoを使用してドキュメントをレンダリングする場合
* レンダリング.内部でpythonを使って描画とかをするのでuv runで実行する
  ```bash
  uv run quarto render my_project.qmd
  uv run quarto render temp2.qmd --output-dir "./report"
  ```