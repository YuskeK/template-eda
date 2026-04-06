# quarto環境構築
* quartoのリリースサイト: https://github.com/quarto-dev/quarto-cli/releases/
  * インストール方法
  ```bash
  # https://zenn.dev/pluck/articles/a2f4b0031ecfef
  wget https://github.com/quarto-dev/quarto-cli/releases/download/v1.2.335/quarto-1.2.335-linux-amd64.deb
  sudo apt install ./quarto-1.2.335-linux-amd64.deb
  ```
  * レンダリング.内部でpythonを使って描画とかをするのでuv runで実行する
  ```bash
  uv run quarto render my_project.qmd
  uv run quarto render temp2.qmd --output-dir "./report"
  ```
* 参考サイト
  * [QuartoとTypstで簡単に美しい論文やレポートを作成する](https://qiita.com/satyuk/items/3760c80b5e383129b8db)
  * [Quarto でレポート執筆（M1 Mac + VSCode）](https://qiita.com/Sangen_u/items/ff7ee6ec1ef2c13f8f99)


# 拡張機能
* Quarto: https://marketplace.visualstudio.com/items?itemName=quarto.quarto
* Live Server: https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer

> [!WARNING]
> Quartoではショートカットキーで`ctrl + shift + k`でHTMLに変換できるが、VSCodeのdelete lineのショートカットと競合する
> `ctrl + shift + p`でshotcutを入力し、`ctrl + shift + k`のquartoのショートカットをオフにする
