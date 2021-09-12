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
npn run serve
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
1. git commit -m "作業内容概要"
2. git checkout develop
3. git pull
4. git checkout feature/xxx-xxx-xxx
5. git merge develop
6. git push feature/xxx-xxx-xxx
※コンフリクトが発生した場合は解消し、1~再度行う
7. GitHubにてpull requestを作成し、developへmergeする
※mergeはsquash and mergeで実行する

### チケット運用
・GitHubのissues/New issueから作成
・担当チケットのAssigneesに自分をセットする
・対応が完了したらissueをクローズする 