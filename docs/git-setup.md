# Git / GitHub 初期設定

職業訓練校 Unity講座（202601期）向けの手順です。

---

## 1. リポジトリを作成する

1. GitHub にログイン
2. **New repository** をクリック
3. リポジトリ名を入力（例：`MyGameProject`）
4. **Private** を選択（推奨）
5. **Create repository** をクリック

---

## 2. Unity プロジェクトを Git 管理する

1. Unity プロジェクトフォルダで `.gitignore` を用意する  
   - [Unity公式 .gitignore](https://github.com/github/gitignore/blob/main/Unity.gitignore) を使用
2. ターミナル（または GitHub Desktop）で以下を実行：

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YourName2026/MyGameProject.git
git push -u origin main
```

---

## 3. 指導講師を Collaborator に追加

1. リポジトリの **Settings** → **Collaborators**
2. 講師の GitHub アカウントを追加
3. 招待メールを承認してもらう

---

## 4. 毎日の作業フロー

```bash
git pull          # 作業前に最新を取得
# Unity で作業…
git add .
git commit -m "5/22 プレイヤー移動を追加"
git push
```

---

## 5. README テンプレートの使い方

1. [個人制作① README テンプレート](../templates/個人制作①_READMEテンプレート.md) を開く
2. 内容をリポジトリ直下の `README.md` にコピー
3. 「制作者情報」「プロジェクト概要」を埋める
4. 毎日「進捗メモ」を1行以上更新して push

---

## よくあるトラブル

| 症状 | 対処 |
|------|------|
| push が拒否される | 先に `git pull` する |
| コンフリクト | 該当ファイルを開いて `<<<<` マーカーを解消 → commit |
| Library が push される | `.gitignore` に Unity テンプレートが入っているか確認 |

---

© 2026 職業訓練校 Unity講座（講師：小西秀明）
