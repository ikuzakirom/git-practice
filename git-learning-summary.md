# 今日のGit学習まとめ 🎉
**日付:** 2026年4月25日（GW）

---

## 1. GitとGitHubの違い

| | Git | GitHub |
|---|---|---|
| 何？ | バージョン管理ツール | クラウド上の保管・共有サービス |
| どこで動く？ | ローカル（自分のPC） | ブラウザ（Web） |
| ネット必要？ | 不要 | 必要 |
| 関係性 | 本体 | Gitの置き場所 |

> 一言で言うと「**Gitが本体、GitHubは置き場所＆共有サービス**」

---

## 2. 今日使ったコマンド一覧

### 初期設定
```bash
git config --global user.name "Kazuki"
git config --global user.email "kazuki.mori024@gmail.com"
```

### リポジトリの作成
```bash
mkdir git-practice   # フォルダを作る
cd git-practice      # フォルダに移動
git init             # Gitリポジトリを初期化する
```

### ファイルの記録（add → commit）
```bash
git status                        # 現在の状態を確認
git add test.txt                  # ステージングする
git commit -m "はじめてのコミット"  # 記録する
```

### ブランチ操作
```bash
git branch feature      # featureブランチを作成
git branch              # ブランチ一覧を確認（*が今いるブランチ）
git checkout feature    # featureブランチに移動
git merge feature       # featureをmasterに合流させる
```

### GitHubへのpush
```bash
git branch -M main                                              # ブランチ名をmainに変更
git remote add origin https://github.com/ikuzakirom/git-practice.git  # GitHubのリポジトリを登録
git push -u origin main                                         # GitHubに送信
```

---

## 3. 今日やったこと（ステップ別）

### Step 1｜Gitの初期設定
- `git --version`でインストール確認 → Git 2.53.0が入っていた
- `git config`でユーザー名とメールアドレスを設定

### Step 2｜リポジトリ作成とはじめてのコミット
- `git-practice`フォルダを作成して`git init`
- `test.txt`を作成して`git add` → `git commit`の流れを体験
- **ステージング**（add）と**コミット**（commit）の違いを理解

### Step 3｜ブランチを体験
- `feature`ブランチを作成して移動
- featureブランチで`feature.txt`を作成・コミット
- masterに戻ると`feature.txt`が見えない → **ブランチの分離**を確認
- `git merge`でfeatureをmasterに合流 → `feature.txt`が見えるようになった

### Step 4｜GitHubにpush
- GitHubでアカウント作成（ユーザー名: ikuzakirom）
- `git-practice`リポジトリをGitHub上に作成
- `git remote add` + `git push`でローカルのコミットをGitHubに送信
- ブラウザでファイルが表示されていることを確認✅

---

## 4. 重要な概念まとめ

**ステージング**
`git add`でコミットに含めるファイルを選ぶ作業。舞台に例えると「出演者を舞台袖に集める」イメージ。

**コミット**
`git commit`で変更を実際に記録する作業。「舞台に上げて記録する」イメージ。

**ブランチ**
作業の分岐。masterに影響を与えずに別の作業ができる。料理で言う「試作品を作る別の鍋」。

**マージ**
ブランチをmasterに合流させること。試作がうまくいったら本番に取り込むイメージ。

**push**
ローカルのコミット履歴をGitHubに送信すること。

---

## 5. 今後学べること

- コンフリクト（複数人が同じファイルを編集したときの競合）の解消
- `git pull`（GitHubから最新の変更を取得する）
- `git rebase`（コミット履歴を整理する）
- Pull Request（チーム開発でのコードレビューの流れ）
- CI/CDとの連携

---

*今日一日でGitの基本操作を全部体験できました！🎉*
