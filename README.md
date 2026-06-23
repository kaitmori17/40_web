# 40_web — ワークスペースの地図

emile の Web 制作ワークスペース。**学習(自分のサイト)** と **受託案件** を大きく分けて管理する。

## 構成
```
40_web/                          ← 管理リポジトリ(このフォルダ。git管理)
├─ CLAUDE.md                     恒久ルール(ワークスペース全体の憲法)
├─ ROADMAP.md                    学習ロードマップ ＝ 自分のサイト専用
├─ GLOSSARY.md                   学習用語集(共有)
├─ README.md                     この地図
├─ gitignore-site-template.txt   各サイト用 .gitignore の雛形
└─ sites/                        ← .gitignore済(中身は各々独立git。管理repoは追跡しない)
   ├─ self/                      自分の統合サイト(1リポジトリ/ハブ多数)※A-2で作成
   └─ clients/                   受託案件(別テーマ・別オーナー)
      └─ milimili/               受託1号(独立git・status.md が正本)
```

## 管理ルールの要点
- **自分のサイト = 1つ**(`sites/self`)。中に複数ハブを増設していく(複数の独立サイトは作らない)。
- **受託 = 別物**(`sites/clients/<案件>`)。各案件は独立リポジトリ + 自前の `status.md`。
- **ドキュメントの住み分け**:
  - 自分の学習・サイトの進捗 → `ROADMAP.md`(将来 `sites/self/status.md`)。
  - 受託の進捗 → 各 `sites/clients/<案件>/status.md`。
  - 用語 → `GLOSSARY.md`(共有)。
  - 恒久ルール → `CLAUDE.md`。
- 各サイトは「1サイト = 1リポジトリ = 1 Vercelプロジェクト」。複数PC同期は git push/pull。
