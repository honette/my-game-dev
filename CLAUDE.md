# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## リポジトリの性質

「AIと一緒に作るゲーム設計」のための Markdown ナレッジベース。現時点でコード・ビルド・テストは存在しない（Phase 0 — Design）。

- `template/` — 新規ゲーム用の雛形。**参照専用・変更禁止**（`template/README.md`）。ユーザーが明示的に許可した場合のみ編集する。
- `my_first_game/` — `template/` を複製した実際のゲームプロジェクト。設計作業はここで行う。
  - `README.md` — 人間とAIの共同設計ルール（最重要。作業前に必ず読む）
  - `01_design/` — 正式な仕様。`00_AI_DEVELOPMENT_PROTOCOL.md` が作業手順とフェーズ定義（Phase 0〜6）、`01`〜`09` が各領域の仕様、`99_PROGRESS.md` が現在フェーズ・次タスク・Decision Log
  - `02_reference/` — 参考作品・分析。仕様へは直接コピーせず、設計原則に変換して `01_design/` に反映する

## 設計作業のルール（`my_first_game/README.md` より）

- **Markdown に記録された内容だけが正式な仕様。** 会話中の合意は、文書に反映されるまで仕様ではない。
- **`TBD` や未定義の重要なゲームデザインを AI が勝手に決めない。** 選択肢・メリット/デメリット・他仕様との矛盾・質問・仮案を提示し、決定は人間が行う。
- 1回の作業は1つの設計テーマに集中する。複数文書にまたがる変更は、先に影響範囲を説明する。
- 詳細化の順序: 概念 → システム → 具体的な数値 → 実装仕様。
- 既存仕様と矛盾する変更は、実装より先に仕様の更新を提案する。仕様を変えたら関連文書の整合性も確認する。
- 人間が承認した内容を文書に反映したら、`99_PROGRESS.md` の Completed / Current Focus / Next Tasks / Decision Log も更新する。
- サイクル: 質問 → 対話 → 決定 → 文書化 → 次の質問。

## 実装フェーズに入ったとき（`00_AI_DEVELOPMENT_PROTOCOL.md` より）

- 一度にゲーム全体を実装しない。小さく実装 → プレイ可能化 → テスト → 修正 → 次へ。
- 完了条件は「コードを書いた」ではなく「意図した体験を実際にプレイできる」こと。
- アセットは既存アセットとの視覚的一貫性を優先し、特定作品の固有デザインをコピーしない。
