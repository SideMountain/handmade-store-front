# handmade-store-front

## 開発手順
### プロジェクトをクローンし最新developから作業用ブランチを切る
```
git clone https://github.com/SideMountain/handmade-store-front.git
```
### セットアップ

```
npm install
```

### vscode の設定
.vscode/setting.jsonに下記を追加

```
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.organizeImports": true,
    "source.fixAll": true
  },
  "editor.formatOnPaste": false,
  "editor.formatOnSave": false,
  "editor.formatOnType": true,
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "vue",
    "typescript"
  ],
}
```

### vscode の拡張

```
code --install-extension dbaeumer.vscode-eslint
code --install-extension emeraldwalk.runonsave
code --install-extension mhutchie.git-graph
code --install-extension msjsdiag.debugger-for-chrome
code --install-extension octref.vetur
code --install-extension esbenp.prettier-vscode
```

### 起動

```
npm run serve
```

### Git関連
#### ブランチ切り方
```
git checkout -b feature/xxx-xxx-xxx
```
#### ブランチ接頭辞
- 新規機能
feature/xxx-xxx-xxx
- 既存機能のサポート
support/xxx-xxx-xxx
- バグ対応
bugfix/xxx-xxx-xxx

#### ブランチ push
1. git add 修正したファイルパス
2. git commit -m "作業内容概要"
3. git checkout develop
4. git pull
5. git checkout feature/xxx-xxx-xxx
6. git merge develop
7. git push feature/xxx-xxx-xxx
※コンフリクトが発生した場合は解消し、1~再度行う
8. GitHubにてpull requestを作成し、developへmergeする
※mergeはsquash and mergeで実行する

### チケット運用
- GitHubのissues/New issueから作成
- 担当チケットのAssigneesに自分をセットする
- 対応が完了したらissueをクローズする 