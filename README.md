# VSCode + LuaLaTeX + bibtex + Textlint テンプレート

## 環境構築

```ps1
# TeX Live インストール (あればスキップ)
choco install texlive

# TLShell TeX Live Manager で拡張インストール

# Node.js インストール (あればスキップ)
winget install OpenJS.NodeJS.LTS

# Node.js ロードのために Powershell をリロード

# Textlint 導入 (初回)
npm init -y
# --save-dev で package.json に追加
npm install --save-dev `
    textlint `
    textlint-plugin-latex2e `
    textlint-filter-rule-comments `
    textlint-rule-preset-ja-technical-writing `
    textlint-rule-preset-jtf-style `
    textlint-rule-preset-ja-spacing `
    @proofdict/textlint-rule-proofdict
npx textlint --init

# Textlint 導入 (2回目以降)
# package.json を参照してインストール
npm install
```

## フォルダ構造

- .vscode
  - extensions.json: 拡張機能一覧
  - settings.json: 各種設定
  - tex.code-snippets: スニペット
- img: 画像保存フォルダ
- .textlintrc: textlint設定
- main.tex: LuaLaTeXテンプレート
- package.json: Node.js環境ファイル
- reference.bib: 参考文献
