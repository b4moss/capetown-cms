---
type: Charter
title: 憲章（charter）
description: 合同会社 知的・自転車の開発方針の最上位取り決め。
tags: [charter]
timestamp: 2026-10-08
---
# 憲章（charter）

**憲章（charter）** は、合同会社 知的・自転車が開発するプロダクトの開発方針の最上位に位置付けられるもの取り決めです。
開発にあたっては、まず憲章を確認し、その方針に従って進めてください。

この憲章は、合同会社 知的・自転車のOSS部門によって[ホスト](https://github.com/b4moss/charter)されています。

各プロジェクトには、この憲章リポジトリ **`main` ブランチの `docs/`**（OKF v0.1）を共有します。かつての `docs` 専用ブランチは使いません。

共有の仕方は、プロジェクトに応じて適切なものを以下から選びます。

1. charter を `remote` に追加し、`charter/main` をマージ（共有対象は `docs/`）。
2. charter を submodule で追加。
3. charter を `remote` に追加し、`subtree` で `docs/` を取り込む。

どの方式を取るかは、プロジェクトに応じてPOが判断をします。具体的なコマンド例はリポジトリルートの [README.md](../../README.md) を参照。

## 憲章の更新

上記のいずれを取ったとしても、各プロジェクトで憲章を更新（上書き・削除）することは禁止します。

憲章は、`charter` のリポジトリが更新されることにより、各プロジェクトで `pull` します。

## 憲章の沿わない事項の扱い

各プロジェクトにおいて、憲章に沿わない事項が出た場合は [/docs/override-charter.md](../override-charter.md)に記載します。

ここに記述された内容は、憲章の内容よりも優先されます。

ここに記述するかどうかは、POが判断します。

## 概要

憲章では、大まかに以下の内容が定められています。

| 文書 | 内容 |
|------|------|
| [tdd.md](./tdd.md) | TDD 方針（氷山パターン、テスト仕様書） |
| [thin-ddd.md](./thin-ddd.md) | 薄い DDD（Controller / Service / Repository / Validation） |
| [git-rule.md](./git-rule.md) | git の運用について |
| [versioning-rule.md](./versioning-rule.md) | バージョンの運用方法について |
| [doc-rule.md](./doc-rule.md) | ドキュメント運用方針 |
| README.md | 本ドキュメント |

プロダクト要件の正本は、各プロジェクトの `docs/README.md`（pillar）および `docs/specs/` とする。`docs/index.md` は OKF 索引のみ。憲章には詰め込まない。

## 記述フォーマット

当憲章を含め、 **OKF v0.1** をベースとした記述でドキュメントを記述します。

## 適用範囲

### すべてのプロジェクト

- TDD
- Gitルール
- バージョニングルール
- ドキュメントルール

### Webアプリケーション / デスクトップアプリケーション

- 薄いDDD

### CLI、パッケージ、ブラウザ拡張

- 薄いDDDは意識しつつ、CRUDを伴わないものはCRUD Traitを採用しなくとも良い。

### 例外

開発初期状態などは、憲章に沿わない状態を許容する。POが適宜判断。
バージョンを重ねるうちに整えていく。

## GitHub / Gitea 等の Issue や Project について

- 開発時は、LLMとの親和性を考え、`docs/`ベースの記述・開発で良い。
- 開発が進むと、複雑化するため、仕様は`docs/`に残しつつ、実装課題やTODOは、Issueを活用していく。
- ただし、Wikiは用いない。（仕様はコードリポジトリを正とするため）


----

以上
