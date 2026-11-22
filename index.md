# パッケージリポジトリのセキュリティ（OpenSSF Securing Software Repositories WG 文書 日本語訳）

OpenSSF の Securing Software Repositories Working Group が [repos.openssf.org](https://repos.openssf.org/) で公開している文書の、非公式な日本語訳です。このワーキンググループは、パッケージリポジトリ（レジストリ）とそれに依存するツールのメンテナーに向けて、セキュリティの成熟度モデル、実装の手引き、提案を公開しています。crates.io、PyPI、npm、RubyGems.org などのパッケージリポジトリに共通する考え方を知るための資料です。

> **ご注意**: この翻訳は OpenSSF や Securing Software Repositories Working Group の確認や公認を受けたものではありません。内容が食い違う場合は原文が優先されます。原文がこの版より後に更新されている場合、訳は古い内容のままです。

## 文書

- [OpenSSF Securing Software Repositories Working Group]({{ '/overview.html' | relative_url }})（原文のトップページ）

### 成熟度モデル

- [パッケージリポジトリのセキュリティの原則]({{ '/principles-for-package-repository-security.html' | relative_url }})（2024 年 2 月）

### 実装の手引き

- [証明（アテステーション）の UI/UX スタイルガイド]({{ '/attestations-style-guide.html' | relative_url }})
  - [スタイルガイド: レベル A - 最低限の要件]({{ '/attestations-style-guide/level-a.html' | relative_url }})
  - [スタイルガイド: レベル AA - 中程度]({{ '/attestations-style-guide/level-aa.html' | relative_url }})
  - [スタイルガイド: レベル AAA - 最高水準の要件]({{ '/attestations-style-guide/level-aaa.html' | relative_url }})
  - [スタイルガイド: UI の詳細]({{ '/attestations-style-guide/ui-details.html' | relative_url }})
  - [スタイルガイド: ドキュメントに関する推奨事項]({{ '/attestations-style-guide/documentation.html' | relative_url }})
  - [PyPI での実装事例]({{ '/attestations-style-guide/pypi-case-study.html' | relative_url }})
- [パッケージ削除ポリシーを作る]({{ '/package-deletion-policies.html' | relative_url }})（2025 年 4 月）
- [すべてのパッケージリポジトリに Trusted Publishers を]({{ '/trusted-publishers-for-all-package-repositories.html' | relative_url }})（2025 年 5 月）
- [すべてのパッケージレジストリにビルド来歴を]({{ '/build-provenance-for-all-package-registries.html' | relative_url }})（2023 年 7 月）

### 提案、調査、そのほかの成果物

- [Homebrew のビルドの来歴とコード署名]({{ '/proposals/build-provenance-and-code-signing-for-homebrew.html' | relative_url }})（2023 年 7 月）

会議の議事録（2022-2023 Meeting Notes）と、リポジトリの `survey/` にある調査（The Package Manager Landscape Survey）は訳していません。スタイルガイドの付属資料（PDF、ZIP、Penpot のファイル）は収録せず、原文へのリンクにしています。

## 出典

- 原文: [repos.openssf.org](https://repos.openssf.org/)（ソースは [ossf/wg-securing-software-repos](https://github.com/ossf/wg-securing-software-repos) の `docs/`）
- 原著者: OpenSSF Securing Software Repositories Working Group（各文書の著者は、それぞれの文書の冒頭に記載されています）
- ライセンス: [Creative Commons Attribution 4.0 International（CC BY 4.0）](https://creativecommons.org/licenses/by/4.0/)
- 訳した版: 2026-11-19 時点（コミット `9c3af8a`）
- 変更点: 日本語への翻訳と、表示用の書式の調整
