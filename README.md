# <リポジトリ名>

> **このリポジトリはテンプレートから作成されている。** 作成後、[リポジトリの作成手順](https://github.com/TUT-ProjectEV/.github-private/blob/main/repository.md#37-リポジトリの作成手順) に従って次を行い、このブロックを削除する。
> - `<>` の部分を書き換え、「主要な文書」の表のファイルを作ったらリンクにする
> - 使わないディレクトリを削除する (例: ソフトウェアを持たないユニットの `firmware/`)
> - `.github/CODEOWNERS` の該当する例を有効にする
> - `system` リポジトリは [ディレクトリ構成](https://github.com/TUT-ProjectEV/.github-private/blob/main/repository.md#システムのリポジトリ-system) が異なるので作り替える

## 概要
| 項目 | 内容 |
| --- | --- |
| ユニット | `<略号>` <ユニット名> |
| 現行車両 | `<車両コード (例: EV26)>` |
| 担当 Team | `@TUT-ProjectEV/<Team 名>` |
| 担当者 | <GitHub アカウント名> |
| 役割 | <このユニットが車両の中で担う役割を2〜3行で> |

## 主要な文書
| 文書 | ファイル | 状態 | 承認済みのタグ |
| --- | --- | --- | --- |
| ユニット要求仕様書 | `docs/requirements/<略号>-REQ-SPEC.md` | 作成中 | |
| ユニット設計書 | `docs/design/<略号>-DESIGN.md` | 作成中 | |
| 基板仕様書 | `docs/design/<基板ID>-SPEC.md` | 作成中 | |
| SW設計書 | `docs/design/<略号>-SW-DESIGN.md` | 作成中 | |
| 結合テスト仕様書 | `docs/test/<略号>-IT-SPEC.md` | 作成中 | |

## 基板・ファームウェア
| 対象 | 現行リビジョン / バージョン | 承認済みのタグ | 備考 |
| --- | --- | --- | --- |
| `<基板ID>` | `revA` | | |
| ファームウェア | | `<車両コード>-FW-v<x.y.z>` | |

## ディレクトリ構成
```
.
├─ README.md                  このファイル
├─ .github
│   ├─ CODEOWNERS
│   ├─ pull_request_template.md
│   └─ ISSUE_TEMPLATE/
├─ docs
│   ├─ requirements/          ユニット要求仕様書
│   ├─ design/                ユニット設計書、基板仕様書、SW設計書、機械取り合い仕様書、図 (*.drawio.svg)
│   ├─ test/                  単体・結合テスト仕様書
│   └─ records
│       └─ <車両コード>/       その車両の記録 (reviews/、test-reports/、photos/)
├─ hardware
│   └─ <基板名>/              KiCad プロジェクト (outputs/ はコミットしない、production/<rev>/ は DR4 承認時)
├─ firmware/                  ソースコード
├─ mechanical/                筐体の図面・加工データ
└─ tools/                     治具、テストスクリプト、模擬環境
```

## 開発環境
| ツール | バージョン |
| --- | --- |
| KiCad | <`system` の README で決めたバージョン> |
| draw.io | |
| ファームウェア開発環境 | |

## 関連する文書
| 文書 | 内容 |
| --- | --- |
| [インタフェース定義書](https://github.com/TUT-ProjectEV/system/tree/main/docs/interface) | このユニットの入出力の正本 |
| [開発フロー](https://github.com/TUT-ProjectEV/.github-private/blob/main/README.md) | V字モデル、ユニット、成果物と ID、安全のルール |
| [開発フェーズ](https://github.com/TUT-ProjectEV/.github-private/blob/main/phases.md) | 各フェーズの入力・実施内容・成果物・完了条件 |
| [デザインレビュー](https://github.com/TUT-ProjectEV/.github-private/blob/main/design-review.md) | DR0〜DR5 の進め方と判定 |
| [リポジトリ運用ルール](https://github.com/TUT-ProjectEV/.github-private/blob/main/repository.md) | ブランチ、Issue、Pull request、タグ |
| [文書テンプレート](https://github.com/TUT-ProjectEV/.github-private/blob/main/README.md#43-テンプレート) | 仕様書・設計書・テスト文書の原本 |
