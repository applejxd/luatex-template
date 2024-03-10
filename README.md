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
    textlint-rule-preset-ja-technical-writing `
    textlint-rule-preset-jtf-style `
    textlint-rule-preset-ja-spacing `
    textlint-rule-spellcheck-tech-word `
    textlint-plugin-latex2e
npx textlint --init

# Textlint 導入 (2回目以降)
# package.json を参照してインストール
npm install
```
