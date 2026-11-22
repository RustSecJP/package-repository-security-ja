# パッケージリポジトリのセキュリティ（OpenSSF Securing Software Repositories WG 文書 日本語訳）

> **これは OpenSSF Securing Software Repositories Working Group が [repos.openssf.org](https://repos.openssf.org/) で公開している文書の、非公式な日本語訳です。** OpenSSF や同ワーキンググループによる確認や公認を受けたものではありません。
>
> **読むのはこちら: https://rustsecjp.github.io/package-repository-security-ja/**
>
> This is an unofficial Japanese translation of the documents published by the OpenSSF Securing Software Repositories Working Group.

OpenSSF Securing Software Repositories Working Group は、パッケージリポジトリ（レジストリ）とそれに依存するツールのメンテナーに向けて、セキュリティの成熟度モデル、実装の手引き、提案を公開しています。このリポジトリでは、次の文書を全文訳しています。

- パッケージリポジトリのセキュリティの原則（Principles for Package Repository Security）
- 証明（アテステーション）の UI/UX スタイルガイド（Style Guide for Attestations UI/UX）と、その下位の 6 ページ
- パッケージ削除ポリシーを作る（Crafting a Package Deletion Policy）
- すべてのパッケージリポジトリに Trusted Publishers を（Trusted Publishers for All Package Repositories）
- すべてのパッケージレジストリにビルド来歴を（Build Provenance for All Package Registries）
- Homebrew のビルドの来歴とコード署名（Build Provenance and Code-signing for Homebrew）
- 原文サイトのトップページ

会議の議事録（2022-2023 Meeting Notes）と、`survey/` にある調査は訳していません。この README は日本語訳の案内だけを載せています（原文リポジトリの README の訳ではありません）。

## 訳した版

| | |
|---|---|
| 原文の版 | 2026-11-19 時点（コミット [`9c3af8a`](https://github.com/ossf/wg-securing-software-repos/commit/9c3af8a36f86ec96001733de6b74c7121acad934)） |
| 翻訳日 | 2026-11-22 |

原文がこの版より後に更新されている場合、訳は古い内容のままです。

## 出典とライセンス

- 原文: https://repos.openssf.org/ （ソース: [ossf/wg-securing-software-repos](https://github.com/ossf/wg-securing-software-repos) の `docs/`）
- 原著者: OpenSSF Securing Software Repositories Working Group。各文書の著者は、それぞれの文書の冒頭に記載されています。
- ライセンス: Creative Commons Attribution 4.0 International（CC BY 4.0） — https://creativecommons.org/licenses/by/4.0/ 。原文リポジトリの [LICENSE](LICENSE) は、OpenSSF の憲章にもとづいて成果物の種類ごとにライセンスを定めており、文書（ソースコード、データ、仕様のどれにも当たらないもの）には CC BY 4.0 が適用されます。この LICENSE は原文のまま収録しています。
- 訳した版: 2026-11-19 時点（コミット 9c3af8a36f86ec96001733de6b74c7121acad934）
- 変更点: 日本語への翻訳。表示用の書式の調整。詳しくは [NOTICE.md](NOTICE.md) にあります。

誤訳の指摘や訳語の提案は、Issue か Pull Request でお願いします。

RustSecJP は非公式のコミュニティです。OpenSSF、Linux Foundation、RustSec、Rust Project、Rust Foundation とは提携していません。
