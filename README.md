# 東栄運輸 業務フロー（観光バス部）

東栄運輸（株）観光バス部の主要業務 6 フローを、Mermaid（BPMN スイムレーン＋シーケンス図）で構造化した Web ビジュアル。

公開: <https://illhhd.github.io/toei-business-flows/>

## 開き方（ローカル）

```sh
open index.html
# or
python3 -m http.server 8000  # → http://localhost:8000/
```

## 構成

| ファイル | 内容 |
|----------|------|
| `index.html` | 6 フローを 1 ページに集約。サイドナビでフロー切替、各フローに 2 ビュー（工程フロー / シーケンス図） |
| `originals/` | 原本資料（PNG 6枚 / DOCX / PPTX） |

## カバーしている業務フロー

1. **予約受付業務** — エージェント問合せ → 見積り → 手配 → 運行確認
2. **運行業務** — 受注 → 配車組 → 出発前 → 出発／到着（中核フロー）
3. **健康診断／適性診断** — 乗務員健康管理サイクル（病院・NASVA 連携）
4. **故障対応** — 事実把握 → 修理（自社 or 日野自動車）→ 復帰
5. **車検／3ヶ月点検** — 法定点検サイクル
6. **車両清掃／コロナ対策** — 日常衛生管理

## 技術スタック

- Mermaid 10（CDN, ESM）— flowchart + sequenceDiagram
- Tailwind CSS（Play CDN）
- Noto Sans JP / Noto Serif JP
- 静的 HTML 単一ファイル（ビルドプロセスなし）

## ソースデータ

- 原本: `originals/toei-manual.docx` / `.pptx`（2020-08）
- フロー図 PNG: `originals/01-reservation.png` 〜 `06-cleaning.png`（2021-03）
- 出典: Studio Saitama × 東栄運輸 DX 推進プロジェクト（2020〜2022）

## デプロイ

GitHub Pages（main ブランチのルート）。`.nojekyll` で Jekyll を無効化。
