{% raw %}
# スタイルガイド: ドキュメントに関する推奨事項 {#style-guide-documentation-recommendations}

効果的なドキュメントでユーザーを支えることは、証明（アテステーション）とは何か、どう使えるのかをユーザーが理解していくうえで鍵になります。

私たちの調査では、証明についての既存のドキュメントは、まったく存在しないか、専門家だけに向けて書かれているかのどちらかでした。この問題に対処し、UI の推奨事項を支えるために、レジストリが証明の利用者に向けた効果的なドキュメントを作る助けとなる、次の原則を提案します。

## 証明をドキュメント化するためのベストプラクティス {#best-practices-for-documenting-attestations}

**証明のドキュメントは、次のことを満たすべきです。**

- パッケージの利用者が証明を理解できるように助ける。証明とは何か、どのように働くのか、どのような限界があるのかを含む

- パッケージの利用者が、ほかのセキュリティ機能や取り組みとの関係の中で証明を理解できるように助ける

- パッケージのメンテナーを、証明を生成するワークフローへ導く

証明のドキュメントが最も効果を発揮するように、ドキュメントの書き手には次の 7 つの原則に従うことをお勧めします。

<h3 id="1-use-key-terms-consistently">1. 重要な用語を一貫して使う</h3>

証明の利用者にとって明確で一貫したものにするために、重要な用語は下の定義どおりに使ってください。この基準を守ることで、パッケージングのエコシステムをまたいだユーザーの混乱を防げます。

来歴（Provenance）
: _定義_: パッケージがどこから来たか
: _すべきこと_: この概念がユーザーにとって新しいかもしれない場面では、見出しや本文でこの用語の意味を明らかにする
: _例_: "Provenance (package origin)"（来歴（パッケージの出どころ））

証明（Attestation）
: _定義_: ソフトウェア成果物についての、署名された事実（またはメタデータ）の表明
: _すべきこと_: 署名された主張を指す一般的な用語として使う。「ビルド来歴証明（Build Provenance Attestation）」のような、より具体的な用語の土台になる

ビルド来歴証明（Build Provenance Attestation）
: _定義_: パッケージが、どのように、いつ、どこでビルドされたかを記述する、特定の種類の証明
: _すべきこと_: この用語を使って、証明とビルド来歴の関係を明らかにする
: _例_: "A build provenance attestation describes how, when, and where a package was built."（ビルド来歴証明は、パッケージが、どのように、いつ、どこでビルドされたかを記述します。）

透明性ログのエントリ（Transparency Log Entry）
: _定義_: 公開台帳に保存された、ビルド来歴証明の改ざんできない記録
: _すべきこと_: 証明がどのように記録されるかを説明するときに「透明性ログのエントリ（transparency log entry）」を使う
: _例_: "Each attestation is recorded in a public ledger as transparency log entry, which is a permanent, auditable record that cannot be changed."（それぞれの証明は、透明性ログのエントリとして公開台帳に記録されます。これは、変更できない、恒久的で監査可能な記録です。）

Verified / verify / verifying（検証済み / 検証する / 検証）
: _定義_: パッケージリポジトリがビルドプラットフォームから証明を受け入れるときに行う処理で、証明の出どころがメンテナーの設定と一致することを確かめるもの。_および_、証明が有効であることを確認するためにユーザーが使える手順
: _すべきこと_: パッケージのアップロード時にリポジトリが自動で行う確認を説明するときは "verified" を使う。ユーザーが証明を確認することを説明するときは "verify" を使う。
: _注意_: ユーザーは "verified" を、パッケージが完全に安全であるという保証として読むことがよくあります（[レベル AA の推奨事項](level-aa.html)を参照）。この用語は、実際に確認した内容に必ず範囲を限定してください。例として [PyPI のケーススタディ](pypi-case-study.html#be-judicious-about-using-verified-checkmark-icons-or-green-styling)を参照してください。
: _例_: "PyPI verifies this attestation at upload time, confirming that the identity matches what the maintainer previously configured for Trusted Publishing."（PyPI はアップロード時にこの証明を検証し、その身元が、メンテナーが Trusted Publishing 用にあらかじめ設定したものと一致することを確認します。） "To manually verify an artifact against its provenance object..."（成果物をその来歴オブジェクトと照らして手動で検証するには……）

<h3 id="2-structure-documentation-around-user-roles">2. ユーザーの役割に沿ってドキュメントを構成する</h3>

パッケージの利用者とメンテナーとでは、証明を含むセキュリティの概念や機能について、必要とする（そして持っている）知識の水準が異なります。

パッケージの利用者向けの内容は、パッケージのメンテナー向けの内容と分け、それぞれの読み手に、関係があって行動に移せる情報を示すべきです。

情報アーキテクチャはユーザーの役割に沿って構成し、"Using This Repository"（利用者向け）や "Publishing Packages"（メンテナー向け）のような、明確な最上位のセクションを使ってください。

<h3 id="3-provide-content-to-help-package-consumers-understand-attestations-within-the-context-of-other-security-features">3. パッケージの利用者が、ほかのセキュリティ機能との関係の中で証明を理解できるような内容を提供する</h3>

証明は、セキュリティというより大きな全体像の一部にすぎません。効果を発揮するには、ドキュメントが証明を文脈の中に位置づけ、ユーザーがリスクについての全体的なメンタルモデルを築けるように助けなければなりません。

パッケージの利用者向けのドキュメントでは、セキュリティの取り組みや機能が、多層防御としてどのように組み合わさって働くかを説明するべきです。ドキュメントは、ユーザーがリスクについて抱く根本的な問いに沿って構成するべきです。

1. ソースコードを信頼できるか？
プロジェクトの活動状況、脆弱性スキャンなどの手がかりを説明する

2. このパッケージはどこから来て、どのように作られたのか？
ビルド来歴と証明を説明する

3. 自分がダウンロードしたファイルは、パッケージリポジトリに置かれているものと同じか？
チェックサムと完全性を説明する

<h3 id="4-warn-package-consumers-that-packages-are-not-secure-by-default">4. パッケージは既定で安全なわけではないと、利用者に警告する</h3>

パッケージの利用者の中には、公式のリポジトリで公開されているパッケージなのだから安全で信頼できる、という誤った思い込みを持っている人がいます。これに対処するために、利用者向けのページに注意書きを入れ、ユーザーをセキュリティのドキュメントへ導いてください。

PyPI の例:
_Warning: Installing packages from PyPI means running third-party code, which carries inherent security risks. Before installing any package, we strongly recommend reading our Package security guide._
（警告: PyPI からパッケージをインストールすることは、第三者のコードを実行することを意味し、それには本質的なセキュリティリスクが伴います。パッケージをインストールする前に、Package security guide を読むことを強くお勧めします。）

<h3 id="5-normalize-secure-by-default-publishing-workflows">5. 既定で安全な公開ワークフローを当たり前のものにする</h3>

ドキュメントは、セキュリティを優先する立場をはっきり取るべきです。どの作業についても、最も安全な方法を、正規の推奨手順として示すべきです。

パッケージの公開についてのドキュメントを書くときは、証明を生成する、最も安全で自動化された公開方法を目立つように取り上げてください。これを最初に、そして最も詳しく説明するワークフローとし、現代の標準として位置づけるべきです。

該当する場合は、推奨するワークフローを使うと来歴の証明が自動的に生成されるという利点があることを、明確にはっきりと述べてください。そうすることで、安全なワークフローを採用する魅力が増します。

証明を生成しない従来の方法には、「非推奨（deprecated）」または「高度な用途向け（for advanced use cases）」とはっきり印を付け、ユーザーがそれらを避けるように導くべきです。

<h3 id="6-explain-common-security-attacks-and-how-they-are-mitigated">6. よくあるセキュリティ攻撃と、その緩和策を説明する</h3>

ユーザーが直面する脅威（たとえばタイポスクワッティング、アカウントの乗っ取り）と、身を守るためにユーザーにできることを、包み隠さず列挙してください。よくある攻撃を緩和するプラットフォーム側の機能を説明し、その中で Trusted Publishing と証明が果たす役割にも触れてください。

個々のパッケージや、パッケージリポジトリ全体のセキュリティに懸念を持ったユーザーのために、分かりやすい報告の窓口を用意してください。

<h3 id="7-be-transparent-about-limitations-and-set-clear-expectations">7. 限界について率直に伝え、期待を明確に設定する</h3>

ドキュメントは、説明するセキュリティの取り組みや機能の範囲と限界について、最初からはっきり述べなければなりません。

証明は来歴（ファイルがどこから来たか）を証明するものであって、コードの安全性（コードにバグや脆弱性がないこと）を保証するものではないと、明確に述べてください。証明を信頼することは、それを発行したツールと権威を暗黙のうちに信頼することを意味する、と説明してください。

下流のツールがどこまで整っているかについても、率直に伝えてください。該当する場合は、一般的なパッケージマネージャーでは証明の自動検証がまだ整っていないことを明示してください。

## ドキュメントの原則を RubyGems.org、PyPI、npm に当てはめる {#applying-documentation-principles-to-rubygemsorg-pypi-and-npm}

RubyGems.org、PyPI、npm が証明のドキュメントのベストプラクティスを取り入れやすくなるように、リポジトリごとに具体的な推奨事項を作りました。それぞれの推奨事項には、ユーザーテストを経たテンプレートが含まれており、新しいドキュメントの作成にも、既存の資料の改訂にも使えます。

RubyGems.org、PyPI、npm には、これらのテンプレートを適切と考える形で使い、改善し、発展させていただきたいと考えています。ほかのパッケージリポジトリも、証明についての独自のドキュメントを作るときの参考として、これらのテンプレートを使えます。

* [RubyGems.org 向けのドキュメントの推奨事項](https://repos.openssf.org/attestations-style-guide/zips/rubygems_attestation_documentation_templates.zip)
* [PyPI 向けのドキュメントの推奨事項](https://repos.openssf.org/attestations-style-guide/zips/pypi_attestation_documentation_templates.zip)
* [npm 向けのドキュメントの推奨事項](https://repos.openssf.org/attestations-style-guide/zips/npm_attestation_documentation_templates.zip)

---

次: [PyPI での実装のケーススタディ](pypi-case-study.html)
{% endraw %}
