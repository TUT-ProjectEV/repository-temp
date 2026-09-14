# <リポジトリ名>

> **このリポジトリはテンプレートから作成されている。** 作成後、[リポジトリの作成手順](https://github.com/TUT-ProjectEV/.github-private/blob/main/repository.md#37-リポジトリの作成手順) に従って次を行い、このブロックを削除する。
> - `<>` の部分を書き換え、「主要な文書」の表のファイルを作ったらリンクにする
> - 使わないディレクトリを削除する (例: ソフトウェアを持たないユニットの `firmware/`)
> - `.github/CODEOWNERS` の該当する例を有効にする
> - `.github/ISSUE_TEMPLATE/inspection.yml` (車検準備) は `system` リポジトリだけで使う。ユニットのリポジトリでは削除する
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
| 文書 | ファイル | 承認済みのタグ |
| --- | --- | --- |
| ユニット仕様書 (要求、構成、機械取り合い、結合テスト項目) | `docs/<略号>-SPEC.md` | |
| 基板仕様書 (基板ごと。SW 設計、単体テスト項目) | `docs/<略号>-PCB-<名称>-SPEC.md` | |

DR・テスト・設計変更の記録は、このリポジトリの Issue (デザインレビュー、テスト記録、設計変更要求) にある。

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
│   ├─ PULL_REQUEST_TEMPLATE/  回路図・アートワークのレビュー (DR3 / DR4) 用
│   └─ ISSUE_TEMPLATE/         作業項目、不具合、設計変更要求、デザインレビュー、テスト記録、車検準備、規則確認
├─ docs
│   ├─ <略号>-SPEC.md          ユニット仕様書
│   ├─ <略号>-PCB-<名称>-SPEC.md  基板仕様書 (基板ごと)
│   ├─ images/                 図 (*.drawio.svg)
│   └─ records
│       └─ <車両コード>/       その車両の記録 (photos/、年度末に書き出した Issue の issues/)
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
| [電装系仕様書](https://github.com/TUT-ProjectEV/system/blob/main/docs/SYS-SPEC.md) | このユニットに割り当てられた電装系要求、電装系の構成 |
| [インタフェース定義書](https://github.com/TUT-ProjectEV/system/blob/main/docs/SYS-IF-SPEC.md) | このユニットの入出力の正本 |
| [開発フロー](https://github.com/TUT-ProjectEV/.github-private/blob/main/README.md) | V字モデル、ユニット、成果物と ID、安全のルール |
| [開発フェーズ](https://github.com/TUT-ProjectEV/.github-private/blob/main/phases.md) | 各フェーズの入力・実施内容・成果物・完了条件 |
| [デザインレビュー](https://github.com/TUT-ProjectEV/.github-private/blob/main/design-review.md) | DR0〜DR5 の進め方と判定 |
| [リポジトリ運用ルール](https://github.com/TUT-ProjectEV/.github-private/blob/main/repository.md) | ブランチ、Issue、Pull request、タグ |
| [文書テンプレート](https://github.com/TUT-ProjectEV/.github-private/blob/main/README.md#43-テンプレート) | ユニット仕様書・基板仕様書の原本 |
