<p align="center">
  <img src="readme.webp" width="200" alt="Logo">
</p>

<h1 align="center"> Takada Laboratory </h1>

<p align="center">
  <img src="https://img.shields.io/badge/Field-Nutrition_%26_Clinical_Medicine-e91e63?style=flat-square" alt="Nutrition & Clinical Medicine">

  <img src="https://img.shields.io/badge/Field-Epidemiology-008080?style=flat-square" alt="Epidemiology">

  <img src="https://img.shields.io/badge/Field-Health_Policy-2c3e50?style=flat-square" alt="Health Policy">

  <img src="https://img.shields.io/badge/Language-R-276DC3?style=flat-square&logo=r&logoColor=white" alt="R">
</p>

同志社女子大学 生活科学部 食物栄養科学科 [臨床病態学研究室](https://daisukegaotian.github.io/labo_settings)のGithub（基本的にオープンなリポジトリ）です。

- 各学生向けの教育用資料は、[Education](https://daisukegaotian.github.io/2026_Labo_semi/education.html)等に公開しています。

- ゼミ課題に関しては、materials/[のディレクトリ以下](https://github.com/DaisukeGaotian/Labo_public/tree/main/materials/2026)や<kbd>年度別privateリポジトリ</kbd>で資料を管理しています。

> [!NOTE]
> このリポジトリは、研究室のゼミ運営・学習資料・成果物を外部に公開するためのものです。
> 「学生向けの配布資料」から、外部の方が「何をどのように勉強しているか」を把握できる資料まで、オープンできる範囲内で幅広く管理します。

---

# 📚 データサイエンス教育の実践指針とカリキュラム・ロードマップ

健康医療分野データサイエンス等の学術的な内容[^1]のみならず、**情報セキュリティに関する考え方、機密情報の扱い、法的な制約や倫理的な観点**を学び、積極的に最新の技術を使いながら、どこへ行ってもこれからの時代を牽引する人材を育成することを目指します。

[^1]:疫学や統計学は、３年生の実習に加えて、４年生前半・大学院前半で半年かけて進めます。教室責任者は[Modern Epidemiology 4th:現代疫学](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.gakujutsu.co.jp/product/978-4-7806-1245-5/&ved=2ahUKEwic19n79ciTAxW3r1YBHZi2BJYQFnoECBsQAQ&usg=AOvVaw2W73smreTGLAW_v7MDsuvm)の分担執筆を行っており、因果推論や疫学に関して体系的な教育を行っています。

## 4年生 前半：RStudio
コマンドラインによる基礎的な文法を学び、データ分析の基礎・可視化・アプリケーション開発の基礎など、**社会人・データサイエンティストとしての基本スキル**を身につけます。  
また、Markdown形式（R Markdown / Quarto）を用いてコードの説明や分析結果の解釈を文書化する方法も実践的に学びます。

> [!TIP]
> コマンドラインの操作経験があるかどうかで、AI時代を生き抜くスキルの幅が大きく変わります。将来的には、AIエージェントとのコミュニケーションがよりスムーズになり、効率的にタスクをこなすことができるようになります。

## 4年生 後半：RStudio / Positron等（＋GitHub Copilot Chat）
前半で身につけた基礎をもとに、オープン情報・機密情報に関するデータ分析の応用や、研究論文の内容を理解して実装する[^2]力を養い、**卒論発表**に臨みます。

[^2]:Scientific writing (論文の書き方)に関しても、継続的に指導を行います。

> [!TIP]
> 基礎を身につけること（調べればわかる知識や考え方）と、目的をもってソフトウェアを使うこと（実践）の間を埋める段階です。

## 大学院：適切にAI エージェントと分担するためのIDE環境の構築
様々な課題に対して自分の力で**大きな枠組みを設計**し、細かい部分をAIエージェントに委任するスタイルを目指します。  
人間が行うこととAIに任せることを適切に分類し、AIエージェントへの指示・監視・修正の技術を実践的に習得します。

> [!TIP]
> **human-in-the-loop** の枠組みで、AIに任せるのではなく人間が監視・微修正する技術の習得を目指します。

---

# 🚀 教室内で使用するツールなど(予定)

下記のもの[^3]はダウンロードして、環境を整えておいてください。

[^3]:将来的には、`Cursor`や`Antigravity`, `Claude Code`等のAIエージェントも積極的に活用していく予定です。

- `Slack`: 研究室内のコミュニケーションツール。質問や雑談など、気軽に使ってください。

- `R/Rstudio`: 各学生のPC内での作業環境。データ分析やコードを書くためのソフトウェアです。

下記は慣れてきたら、積極的に活用を検討していきます。

- `Git/Github`: 研究室内共有の作業ノート。ゼミで勉強した内容やコードを保存[^4]する場所です。

[^4]:いずれ説明しますが、アップしていいものとダメなものがあります。Github Educationの特典を受けているので、Github Copilot Chatなども併用していく予定です

- `shinyapps.io`: Rで作ったアプリを公開するためのサービス。研究室内で作成したアプリを外部に公開する際に使用します。

> [!IMPORTANT]
> AIの学習に使われないための設定を忘れないようにしましょう。<br>
> GitHub Copilotを使用する場合は、
> [GitHub CopilotのAIプライバシー](https://github.com/settings/copilot/features) -> Privacy -> Allow GitHub to use my data for AI model training を、
> `Disabled`に設定してください。<br>
> Antigravityでも、
> Antigravity -> 基本設定 -> Antigravity Settings -> Account -> Enable Telemetry
> を、できないように(左に)しておきましょう。

---

# 🔒 各年度プライベートリポジトリとの使い分けについて

> [!IMPORTANT]
> このリポジトリとは違い、`Labo_20**students_**`はprivateリポジトリで、ゼミ生の成果物や非公開の資料を指導しながら管理するためのものです。

いきなり外部に公表するのに抵抗があると思うので、まずは`Labo_20**students_**`で`commit`、`push`、`pull`などの経験を積み、一通り様々な経験をした段階で`Labo_public`に公表する運用を考えています。

> [!CAUTION]
> 絶対にやってはいけないこと：
> HTMLファイル内や、Publicリポジトリ内のコードに、サーバーの`パスワード`や`APIキー`を直接書き込むことは避けてください。
> これらは公開された瞬間に悪用されるリスクがあります。

---

# 📁 ディレクトリ構造(予定)

```
Labo_public/
├── README.md                     # このファイル（リポジトリ概要・教育方針）
├── .gitignore
│
├── docs/                         # ゼミ運営の中心となる公開文書
│   ├── curriculum.md             # カリキュラム方針・学習ロードマップ(予定)
│   └── tools.md                  # 使用ツール一覧と導入ガイド(予定)
│
├── materials/                    # 学年・年度ごとの配布資料（毎年更新予定）
│   ├── README.md
│   └── 2026/
│
├── templates/                    # Rmd/Quarto テンプレート（再利用可能）
│
└── data/                         # 公開可能なサンプルデータ

```
> [!NOTE]
> `_private/` フォルダ（`.gitignore` で除外）は各学生のPC(ローカル環境)にのみ存在し、非公開のドキュメント・チェックスクリプト等を管理しています。
