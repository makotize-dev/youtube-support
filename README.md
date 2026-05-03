# YouTube チャンネル運営サポート

**対象チャンネル：** [hi-to0](https://youtube.com/@hi-to0)
**担当：** 安河内（事務作業全般）

歌ってみた・ゲーム配信などのコンテンツを継続して届けるため、**制作（友人）と事務（安河内）を分業**するためのリポジトリ。当面の主担当業務は **次に歌う候補曲の著作権確認とインスト確保**。

---

## 🔗 状況確認画面（友人向け）

候補曲の進捗・判定結果はここで確認できる：

**https://makotize-dev.github.io/youtube-support/**

ブックマーク推奨。`docs/songs.csv` の更新が push されると自動で反映される。

---

## 📖 作業手順書

候補曲を受け取ってから判定結果を返すまでの全手順：

→ **[docs/workflow.md](./docs/workflow.md)**

著作権の判定基準など参考資料：

→ [docs/copyright-guide.md](./docs/copyright-guide.md)

---

## フォルダ構成

| パス | 内容 |
|---|---|
| `docs/songs.csv` | 全曲の状態管理（候補・進行中・投稿済みを一元） |
| `docs/index.html` | 友人向け状況確認画面（GitHub Pages から配信） |
| `docs/workflow.md` | 作業手順書（SOP） |
| `docs/copyright-guide.md` | 著作権確認の参考資料 |
| `candidates/_template.md` | 詳細な調査メモが必要な曲用のテンプレート |
| `candidates/<曲名>.md` | 個別の調査メモ（必要な曲だけ作成） |
| `_later/` | 当面後回しにしている素材（templates・analytics・coconala・twitch・旧HTML） |

インスト音源は **Google Drive `hi-to0_inst/`** で管理（リポジトリには入れない）。

---

## 作業の入口

1. LINE で友人から候補曲を受信
2. [docs/workflow.md](./docs/workflow.md) のステップに沿って `docs/songs.csv` を更新
3. 必要に応じて `candidates/<曲名>.md` を作成
4. インストを Google Drive にアップ
5. `git push` → 友人に画面 URL を通知

---

## `_later/` の意図

`_later/` 配下のファイルは **「いま手をつけないが、将来的にやる」** ものを意図的に退避している場所。削除ではない。

- `analytics/` — 月次統計
- `coconala/` — MIX出品ページ下書き
- `twitch/` — Twitch 配信開設チェックリスト
- `songs-template/` — 投稿準備時に使う説明文・タグ・SNS投稿テンプレ
- `index.html` / `songs.html` — 旧ダッシュボード（`docs/index.html` で置換）

候補曲調査の運用が安定してから、必要なものから順に復帰させる方針。
