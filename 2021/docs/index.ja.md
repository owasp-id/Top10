# OWASP Top 10 2021の紹介

OWASP トップ 10 の最新版へようこそ! OWASP トップ 10 2021年版は、グラフィックデザインが一新され、1ページのインフォグラフィックになっています。インフォグラフィックは、ホームページから入手でき、印刷することができます。

今回のトップ10の作成にあたって、貴重な時間やデータを提供してくださったすべての皆さんに感謝します。皆様のご協力なくしては、OWASP トップ 10 2021年版は存在し得ません。**本当に、感謝いたします**。

## 2021年版トップ10の変更点

2021年版トップ10では、3つの新しいカテゴリー、4つのカテゴリーの名称とスコープの変更がありました。統合されたものもいくつかあります。

<img src="./assets/image1.png" style="width:6.5in;height:1.78889in" alt="Mapping of the relationship between the Top 10 2017 and the new Top 10 2021" />

**A01:2021-アクセス制御の不備** は、5位から順位を上げました。94%のアプリケーションで、何らかの形でアクセス制御の不備が確認されています。また、「アクセス制御の欠陥」にあたる34件のCWEは、他のカテゴリーよりもアプリケーションで多く発生しています。

**A02:2021-暗号化の失敗** は、ひとつ順位を上げて2位になっています。
以前は、「機微な情報の露出」と呼ばれていましたが、これは根本的な原因というより幅広くみられる症状と言えます。ここでは、機密データの漏えいやシステム侵害に多く関連する、暗号技術にまつわる失敗に焦点を当てています。

**A03:2021-インジェクション** は、3位に下がっています。94%のアプリケーションで、何らかのインジェクションに関する問題が確認されており、このカテゴリにあたる33のCWEは、アプリケーションでの発生数が2番目に多く見られます。今回から、クロスサイトスクリプティングは、このカテゴリに含まれています。

**A04:2021-安全が確認されない不安な設計** は、2021年に新設されたカテゴリーで、設計上の欠陥に関するリスクに焦点を当てています。一業界として、我々が純粋に「シフトレフト」することを望むのであれば、脅威モデリングや、安全な設計パターンと原則、また、リファレンス・アーキテクチャをもっと利用していくことが必要です。

**A05:2021-セキュリティの設定ミス** は、前回の6位から順位を上げました。アプリケーションの90％には何らかの設定ミスが見られます。高度な設定が可能なソフトウェアへの移行が進む中で、このカテゴリーの順位が上がったことは当然と言えます。以前の、XML外部エンティティ参照(XXE)のカテゴリーは、このカテゴリーに含まれています。

**A06:2021-脆弱で古くなったコンポーネント** は、以前は「既知の脆弱性のあるコンポーネントの使用」というタイトルでした。この問題は、業界調査では2位であり、データ分析によってトップ10に入るだけのデータもありました。このカテゴリーは2017年の9位から順位を上げました。これは、テストやリスク評価に苦労する、よく知られた問題です。また、含まれるCWEにあたるCVEのない、唯一のカテゴリであるため、デフォルトのエクスプロイトとインパクトの重みは5.0としてスコアに反映されています。

**A07:2021-識別と認証の失敗** 以前、第2位で「認証の不備」と呼ばれていましたが、この版では、識別の失敗に関連するCWEをより多く含む意味合いのカテゴリとなっています。このカテゴリーは依然としてトップ10に示すべき重要な項目ですが、標準化されたフレームワークの利用が進んだことが功を奏しているようです。

**A08:2021-ソフトウェアとデータの整合性の不具合** これは2021年に新設されたカテゴリーで、ソフトウェアの更新、重要なデータを、CI/CDパイプラインにおいて整合性を検証せずに見込みで進めることによる問題にフォーカスしています。CVE/CVSSのデータから最も重大な影響を受けたものの1つが、このカテゴリーの10のCWEにマッピングされています。2017年の「安全でないデシリアライゼーション」は、このカテゴリーの一部となりました。

**A09:2021-セキュリティログとモニタリングの失敗**  は、従来は「ロギングとモニタリングの不足」でしたが、業界の調査（第3位）から追加され、従来の第10位からランクアップしました。このカテゴリは、より多くの種類の失敗を含むように拡張されています。これは、テストが困難なものであり、かつ、CVE/CVSSのデータにはあまり反映されないものです。とはいえ、このカテゴリーで失敗が起きると、可視性、インシデントアラート、フォレンジックなどに直接影響を与える可能性があります。

**A10:2021-サーバーサイド・リクエスト・フォージェリ** は、業界の調査（第1位）から追加されたものです。調査データからわかることは、よくあるテストより広範な範囲において、問題の発生率は比較的低いものの、問題が起きた場合のエクスプロイトとインパクトは平均以上のものとなり得ます。このカテゴリは、現時点でデータとして現れるものではありませんでしたが、複数の業界の専門家により重要との示唆を得たシナリオとして反映しています。

## 方法論

今回のトップ10は、これまで以上にデータを重視していますが、やみくもにデータを重視しているわけではありません。10項目のうち8項目は提供されたデータから、2項目は業界調査から高いレベルで選びました。こうすることにはひとつの根本的な理由があります。提供されたデータを見ることは、過去を見ることを意味している、ということです。アプリケーションセキュリティのリサーチャーが新しい脆弱性や、それをテストする新しい方法を見つけるのには時間がかかります。これらのテストをツールやプロセスに組み込むには時間がかかります。こうした弱点を広く確実にテストできるようになるまでには、何年もかかってしまうことでしょう。そこで、データではわからないような本質的な弱点は何かということについては、業界の第一線で活躍されている方々にお聞きすることでバランスをとる、というわけです。

トップ10を継続的に成熟させるために私たちが採用した、重要な変更点がいくつかあります。

### How the categories are structured

A few categories have changed from the previous installment of the OWASP
Top Ten. Here is a high-level summary of the category changes.

Previous data collection efforts were focused on a prescribed subset of
approximately 30 CWEs with a field asking for additional findings. We
learned that organizations would primarily focus on just those 30 CWEs
and rarely add additional CWEs that they saw. In this iteration, we
opened it up and just asked for data, with no restriction on CWEs. We
asked for the number of applications tested for a given year (starting
in 2017), and the number of applications with at least one instance of a
CWE found in testing. This format allows us to track how prevalent each
CWE is within the population of applications. We ignore frequency for
our purposes; while it may be necessary for other situations, it only
hides the actual prevalence in the application population. Whether an
application has four instances of a CWE or 4,000 instances is not part
of the calculation for the Top 10. We went from approximately 30 CWEs to
almost 400 CWEs to analyze in the dataset. We plan to do additional data
analysis as a supplement in the future. This significant increase in the
number of CWEs necessitates changes to how the categories are
structured.

We spent several months grouping and categorizing CWEs and could have
continued for additional months. We had to stop at some point. There are
both *root cause* and *symptom* types of CWEs, where *root cause* types
are like "Cryptographic Failure" and "Misconfiguration" contrasted to
*symptom* types like "Sensitive Data Exposure" and "Denial of Service."
We decided to focus on the root cause whenever possible as it's more
logical for providing identification and remediation guidance. Focusing
on the root cause over the symptom isn't a new concept; the Top Ten has
been a mix of *symptom* and *root cause*. CWEs are also a mix of
*symptom* and *root cause*; we are simply being more deliberate about it
and calling it out. There is an average of 19.6 CWEs per category in
this installment, with the lower bounds at 1 CWE for
*A10:2021-Server-Side Request Forgery (SSRF)* to 40 CWEs in
*A04:2021-Insecure Design*. This updated category structure offers
additional training benefits as companies can focus on CWEs that make
sense for a language/framework.

### How the data is used for selecting categories

In 2017, we selected categories by incidence rate to determine
likelihood, then ranked them by team discussion based on decades of
experience for Exploitability, Detectability (also likelihood), and
Technical Impact. For 2021, we want to use data for Exploitability and
Impact if possible.

We downloaded OWASP Dependency Check and extracted the CVSS Exploit, and
Impact scores grouped by related CWEs. It took a fair bit of research
and effort as all the CVEs have CVSSv2 scores, but there are flaws in
CVSSv2 that CVSSv3 should address. After a certain point in time, all
CVEs are assigned a CVSSv3 score as well. Additionally, the scoring
ranges and formulas were updated between CVSSv2 and CVSSv3.

In CVSSv2, both Exploit and Impact could be up to 10.0, but the formula
would knock them down to 60% for Exploit and 40% for Impact. In CVSSv3,
the theoretical max was limited to 6.0 for Exploit and 4.0 for Impact.
With the weighting considered, the Impact scoring shifted higher, almost
a point and a half on average in CVSSv3, and exploitability moved nearly
half a point lower on average.

There are 125k records of a CVE mapped to a CWE in the NVD data
extracted from OWASP Dependency Check, and there are 241 unique CWEs
mapped to a CVE. 62k CWE maps have a CVSSv3 score, which is
approximately half of the population in the data set.

For the Top Ten, we calculated average exploit and impact scores in the
following manner. We grouped all the CVEs with CVSS scores by CWE and
weighted both exploit and impact scored by the percentage of the
population that had CVSSv3 + the remaining population of CVSSv2 scores
to get an overall average. We mapped these averages to the CWEs in the
dataset to use as Exploit and Impact scoring for the other half of the
risk equation.

## Why not just pure statistical data?

The results in the data are primarily limited to what we can test for in
an automated fashion. Talk to a seasoned AppSec professional, and they
will tell you about stuff they find and trends they see that aren't yet
in the data. It takes time for people to develop testing methodologies
for certain vulnerability types and then more time for those tests to be
automated and run against a large population of applications. Everything
we find is looking back in the past and might be missing trends from the
last year, which are not present in the data.

Therefore, we only pick eight of ten categories from the data because
it's incomplete. The other two categories are from the industry survey.
It allows the practitioners on the front lines to vote for what they see
as the highest risks that might not be in the data (and may never be
expressed in data).

## Why incidence rate instead of frequency?

There are three primary sources of data. We identify them as
Human-assisted Tooling (HaT), Tool-assisted Human (TaH), and raw
Tooling.

Tooling and HaT are high-frequency finding generators. Tools will look
for specific vulnerabilities and tirelessly attempt to find every
instance of that vulnerability and will generate high finding counts for
some vulnerability types. Look at Cross-Site Scripting, which is
typically one of two flavors: it's either a more minor, isolated mistake
or a systemic issue. When it's a systemic issue, the finding counts can
be in the thousands for an application. This high frequency drowns out
most other vulnerabilities found in reports or data.

TaH, on the other hand, will find a broader range of vulnerability types
but at a much lower frequency due to time constraints. When humans test
an application and see something like Cross-Site Scripting, they will
typically find three or four instances and stop. They can determine a
systemic finding and write it up with a recommendation to fix on an
application-wide scale. There is no need (or time) to find every
instance.

Suppose we take these two distinct data sets and try to merge them on
frequency. In that case, the Tooling and HaT data will drown the more
accurate (but broad) TaH data and is a good part of why something like
Cross-Site Scripting has been so highly ranked in many lists when the
impact is generally low to moderate. It's because of the sheer volume of
findings. (Cross-Site Scripting is also reasonably easy to test for, so
there are many more tests for it as well).

In 2017, we introduced using incidence rate instead to take a fresh look
at the data and cleanly merge Tooling and HaT data with TaH data. The
incidence rate asks what percentage of the application population had at
least one instance of a vulnerability type. We don't care if it was
one-off or systemic. That's irrelevant for our purposes; we just need to
know how many applications had at least one instance, which helps
provide a clearer view of the testing is findings across multiple
testing types without drowning the data in high-frequency results.

## What is your data collection and analysis process?

We formalized the OWASP Top 10 data collection process at the Open
Security Summit in 2017. OWASP Top 10 leaders and the community spent
two days working out formalizing a transparent data collection process.
The 2021 edition is the second time we have used this methodology.

We publish a call for data through social media channels available to
us, both project and OWASP. On the [OWASP Project
page](https://owasp.org/www-project-top-ten/#div-data_2020), we list the
data elements and structure we are looking for and how to submit them.
In the [GitHub
project](https://github.com/OWASP/Top10/tree/master/2020/Data), we have
example files that serve as templates. We work with organizations as
needed to help figure out the structure and mapping to CWEs.

We get data from organizations that are testing vendors by trade, bug
bounty vendors, and organizations that contribute internal testing data.
Once we have the data, we load it together and run a fundamental
analysis of what CWEs map to risk categories. There is overlap between
some CWEs, and others are very closely related (ex. Cryptographic
vulnerabilities). Any decisions related to the raw data submitted are
documented and published to be open and transparent with how we
normalized the data.

We look at the eight categories with the highest incidence rates for
inclusion in the Top 10. We also look at the industry survey results to
see which ones may already be present in the data. The top two votes
that aren't already present in the data will be selected for the other
two places in the Top 10. Once all ten were selected, we applied
generalized factors for exploitability and impact; to help rank the Top
10 in order.

## Data Factors

There are data factors that are listed for each of the Top 10
Categories, here is what they mean:

-   *CWEs Mapped*: The number of CWEs mapped to a category by the Top 10
    team.

-   *Incidence Rate*: Incidence rate is the percentage of applications
    vulnerable to that CWE from the population tested by that org for
    that year.

-   (Testing) *Coverage*: The percentage of applications tested by all
    organizations for a given CWE.

-   *Weighted Exploit*: The Exploit sub-score from CVSSv2 and CVSSv3
    scores assigned to CVEs mapped to CWEs, normalized, and placed on a
    10pt scale.

-   *Weighted Impact*: The Impact sub-score from CVSSv2 and CVSSv3
    scores assigned to CVEs mapped to CWEs, normalized, and placed on a
    10pt scale.

-   *Total Occurrences*: Total number of applications found to have the
    CWEs mapped to a category.

-   *Total CVEs*: Total number of CVEs in the NVD DB that were mapped to
    the CWEs mapped to a category.

## Category Relationships from 2017

There has been a lot of talk about the overlap between the Top Ten
risks. By the definition of each (list of CWEs included), there really
isn't any overlap. However, conceptually, there can be overlap or
interactions based on the higher-level naming. Venn diagrams are many
times used to show overlap like this.

<img src="./assets/image2.png" style="width:4.31736in;height:3.71339in" alt="Diagram Description automatically generated" />

The Venn diagram above represents the interactions between the Top Ten
2017 risk categories. While doing so, a couple of essential points
became obvious:

1.  One could argue that Cross-Site Scripting ultimately belongs within
    Injection as it's essentially Content Injection. Looking at the 2021
    data, it became even more evident that XSS needed to move into
    Injection.

2.  The overlap is only in one direction. We will often classify a
    vulnerability by the end manifestation or "symptom," not the
    (potentially deep) root cause. For instance, "Sensitive Data
    Exposure" may have been the result of a "Security Misconfiguration";
    however, you won't see it in the other direction. As a result,
    arrows are drawn in the interaction zones to indicate which
    direction it occurs.

3.  Sometimes these diagrams are drawn with everything in *A06:2021
    Using Components with Known Vulnerabilities*. While some of these
    risk categories may be the root cause of third-party
    vulnerabilities, they are generally managed differently and with
    different responsibilities. The other types are typically
    representing first-party risks.

# Thank you to our data contributors

The following organizations (along with some anonymous donors) kindly
donated data for over 500,000 applications to make this the largest and
most comprehensive application security data set. Without you, this
would not be possible.

| | | | |
| :---: | :---: | :---: | :---: |
| AppSec Labs | GitLab | Micro Focus | Sqreen |
| Cobalt.io | HackerOne | PenTest-Tools | Veracode |
| Contrast Security | HCL Technologies | Probely | WhiteHat (NTT) |

## Thank you to our sponsors

The OWASP Top 10 2021 team gratefully acknowledge the financial support of Secure Code Warrior and Just Eat.

[![Secure Code Warrior](assets/securecodewarrior.png){ width="256" }](https://securecodewarrior.com)    

[![Just Eats](assets/JustEat.png){ width="256" }](https://www.just-eat.co.uk/)