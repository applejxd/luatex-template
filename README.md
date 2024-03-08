# VSCode + LuaLaTeX + bibtex + Textlinkt テンプレート

## 環境構築

```ps1
# Node.js インストール (あればスキップ)
winget install OpenJS.NodeJS.LTS

# Powershell をリロード

# Textlint 導入
npm init -y
npm install --save-dev `
    textlint `
    textlint-rule-preset-ja-spacing `
    textlint-rule-preset-ja-technical-writing `
    textlint-rule-spellcheck-tech-word `
    textlint-plugin-latex2e
npx textlint --init

```
