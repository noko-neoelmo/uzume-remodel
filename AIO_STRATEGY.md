# UZUME AIO（AI Overview Optimization）戦略書

## 概要

本戦略は、UZUMEのジュエリーリモデル・サイズ直しサービスに対し、
AI検索エンジン（Google AI Overviews, ChatGPT, Perplexity, Gemini等）から
適切に発見・推薦されるための包括的な施策をまとめたものです。

### なぜAIOが重要か（調査データ）

- AI Overviewsは全Google検索の **13.1%** に表示（2025年3月、増加傾向）
- AI Overviewsにより情報検索クエリのオーガニックCTRが最大 **61%低下**
- AI Overview引用の **76%** がGoogle検索トップ10のページから
- ゼロクリック検索が56%→ **69%** に上昇（2025年5月）
- Gartnerは2026年までに従来型検索量が **25%減少**、2028年までにオーガニックトラフィックが **50%以上減少** と予測
- AIエージェントが全オーガニック検索活動の約 **33%** を占める
- GPTBotのトラフィックは2024年5月〜2025年5月で **305%増加**

**根本的な変化：** 10個の青いリンクの中のポジション争いではなく、LLMが1つの回答で引用する **2〜7サイト** に選ばれる競争になった。

---

## エージェント体制（Agent Team）

以下の5つのサブエージェントチームで分担して対策を行います。

### Agent 1: Technical AIO（技術的AI最適化）✅ 実装済
**担当領域:** サイト内の技術的なAI可読性向上
- `llms.txt` の作成・配置（AI向けサイト説明ファイル）
- 構造化データ（JSON-LD）の強化・拡充
- `robots.txt` でのAIクローラー許可設定
- `sitemap.xml` の生成
- canonical URL の設定
- メタタグ強化（OGP, Twitter Card, description等）
- Vercel headers設定（llms.txtのContent-Type）

### Agent 2: Content Strategy（コンテンツ戦略）
**担当領域:** AI に引用されやすいコンテンツの設計

#### 核心原則
- **Answer-First（回答ファースト）:** 各セクションの冒頭に1-2文の直接回答を置く（Snippet Bait）
- **低パープレキシティ:** 平易で構造化された明確な言葉を使う。AIモデルは予測しやすいテキストを優先する
- **40-60語の段落回答:** Featured Snippet抽出に最適な長さ
- **オリジナル情報:** AIが生成できない一次情報（実体験、ケーススタディ）が最も価値が高い

#### note.com記事戦略
**note.comがAIOに強い理由（VALUES社調査より）:**
- 大規模な更新頻度によりGoogleのインデックス速度が速い
- 広告がないことでユーザー行動指標が良好
- ドメイン全体の権威性から個別記事も恩恵を受ける
- LLMの事前学習データに含まれやすい大規模サイト
- ChatGPTからnote.comへのリファラルトラフィックが5ヶ月で **約4倍** に成長

**注意:** 2025年10月にnote記事約20万件がGoogleからデインデックスされた事例あり。品質とオリジナリティが最重要。

#### 必須記事（優先度高）
1. **「ジュエリーリモデルとは？リフォームとの違いを徹底解説」**
   - ターゲットKW: ジュエリーリモデル, ジュエリーリフォーム 違い
   - AI引用狙い: 定義・比較の明確な回答
   - 記事構成: 冒頭に結論→違いの表→各メリット・デメリット→UZUMEの事例

2. **「指輪のサイズ直し完全ガイド｜費用・期間・方法を解説」**
   - ターゲットKW: 指輪 サイズ直し, リング サイズ変更
   - AI引用狙い: 具体的な料金・期間・手順
   - 記事構成: 結論（3万円・1ヶ月）→方法比較→素材別注意点→UZUMEの特徴

3. **「甲府の宝飾産業700年の歴史とUZUMEの職人技」**
   - ターゲットKW: 甲府 宝飾, ジュエリー 職人
   - AI引用狙い: E-E-A-T（専門性・権威性）の確立
   - 記事構成: 甲府の歴史→現代の技術→UZUMEの職人紹介→具体的な加工工程

4. **「婚約指輪・結婚指輪のリモデル事例集」**
   - ターゲットKW: 婚約指輪 リフォーム, エンゲージリング リモデル
   - AI引用狙い: 具体的事例・ビフォーアフター
   - 記事構成: 代表事例3-5件→各事例の背景・デザイン意図・完成品→費用感

#### 推奨記事（中期）
5. 「ジュエリー素材買取の仕組みと活用法」
6. 「オンラインでジュエリーリフォームを依頼する方法」
7. 「宝石の鑑定書とは？無料鑑定の価値」
8. 「大切なジュエリーを受け継ぐということ」

#### note記事の書き方テンプレート
```
■ タイトル: ターゲットKWを含む（30文字以内）
■ 冒頭: 1-2文で結論を述べる（AI引用の対象）
■ H2見出し: 質問形式で構造化
■ 本文: 具体的な数値（料金、期間、素材名）を必ず含める
■ 内部リンク: UZUMEサイトへのリンクを2-3箇所
■ CTA: LINE相談への誘導
■ 文字数: 3,000-5,000文字（充実した内容）
■ 更新: 月1回以上の定期更新
```

### Agent 3: Entity & Authority Building（エンティティ構築）
**担当領域:** AI が「UZUME」をエンティティとして認識するための施策

#### なぜエンティティ構築が重要か
AIは **クロスプラットフォームの検証** を重視する。孤立したコンテンツはAIに認識されにくい。

#### 具体的アクション
- **Google Business Profile** の作成・最適化（住所: 南青山2-5-17）
- **Wikipedia** ページの作成検討（Wikipedia掲載はAI認識に極めて重要）
- 業界メディア・**プレスリリース** 戦略
- **SNS（Instagram, X）** でのブランドシグナル強化
- `sameAs` プロパティでの各プラットフォーム紐付け（実装済）
- **口コミ・レビュー** 管理（AIはレビュー感情を推薦判断に活用）
- **Yahoo!知恵袋、Qiita、Hatena Blog** での言及

### Agent 4: External Platform（外部プラットフォーム対策）
**担当領域:** UZUME への動線をAIが生成するための外部施策
- note.com での定期的な専門記事投稿（Agent 2と連携）
- Googleマップ口コミ対策
- 比較サイト・まとめサイトへの掲載
- 「おすすめ」リスト記事への掲載依頼
- 業界フォーラム・コミュニティでの存在感構築

### Agent 5: Monitoring & Iteration（モニタリング）
**担当領域:** AIO対策の効果測定と改善

#### 定期チェック項目
- [ ] ChatGPTで「ジュエリーリモデル おすすめ」を検索→UZUME言及を確認
- [ ] Perplexityで「指輪 サイズ直し オンライン」を検索→UZUME言及を確認
- [ ] Google AI Overviewでの表示状況確認
- [ ] 構造化データの [Rich Results Test](https://search.google.com/test/rich-results) でバリデーション
- [ ] Search Console でのパフォーマンス追跡
- [ ] GA4でAIリファラルトラフィック計測（openai.com, perplexity.ai等からの流入）
- [ ] 競合のAIO対策状況の調査

---

## 技術的実装詳細

### 1. llms.txt
AI（LLM）がサイトを理解するための構造化テキストファイル。
- Jeremy Howard（FastAI創設者）が2024年9月に提案した標準
- **84万4,000以上のサイト** が実装済（2025年10月）
- Anthropic, Cloudflare, Stripe等の大手も採用
- 現時点で主要AIプラットフォームが公式に読み取りを確認したわけではないが、実装コストが低くデメリットがないため推奨

### 2. 構造化データ（JSON-LD）強化
- Organization スキーマ（sameAs, knowsAbout付き）→ エンティティ認識
- WebSite スキーマ → サイト全体の情報提供
- 既存の LocalBusiness, FAQPage, HowTo, Service を維持
- **構造化データの効果:** AI要約でのブランド表示が **36%増加**、引用が **4.1倍** に（調査データ）

### 3. メタタグ・SEO強化
- Twitter Card メタタグ追加
- canonical URL 設定
- og:url, og:image, og:locale, og:site_name 追加

### 4. robots.txt
AIクローラーの種類と推奨設定:

| クローラー | プラットフォーム | 用途 | 設定 |
|-----------|----------------|------|------|
| GPTBot | OpenAI | モデル学習 | ✅ Allow |
| OAI-SearchBot | OpenAI | リアルタイム検索（ChatGPT） | ✅ Allow（重要） |
| ChatGPT-User | OpenAI | ユーザー起動のブラウジング | ✅ Allow |
| ClaudeBot | Anthropic | クロール | ✅ Allow |
| PerplexityBot | Perplexity | リアルタイム検索 | ✅ Allow |
| Google-Extended | Google | AI学習（Gemini） | ✅ Allow |
| Googlebot | Google | 検索 + AI Overviews | ✅ Allow |
| Applebot-Extended | Apple | Apple Intelligence | ✅ Allow |

### 5. sitemap.xml
全ページのURL・更新日・優先度を記載。

### 6. Vercel設定
llms.txtに適切なContent-Typeヘッダーを設定。

---

## KPI

| 指標 | 目標 | 計測方法 |
|------|------|---------|
| AI Overview表示率 | UZUME関連クエリで表示 | 手動検索 |
| ChatGPT/Perplexity言及率 | 「ジュエリーリモデル」でUZUME言及 | 手動検索 |
| Rich Resultsテスト | 合格率100% | Google Rich Results Test |
| AI経由サイト流入 | 月次増加 | GA4リファラル |
| note記事流入 | 月次増加 | GA4 |
| LINE友達追加数 | 月次増加 | LINE管理画面 |

---

## 実装ステータス

| 施策 | 対象サイト | ステータス |
|------|-----------|-----------|
| llms.txt | 両サイト | ✅ 実装済 |
| 構造化データ強化（Organization, WebSite） | 両サイト | ✅ 実装済 |
| メタタグ強化（OGP, Twitter Card, canonical） | 両サイト | ✅ 実装済 |
| robots.txt（全AIクローラー許可） | 両サイト | ✅ 実装済 |
| sitemap.xml | 両サイト | ✅ 実装済 |
| Vercel headers設定 | 両サイト | ✅ 実装済 |
| note記事作成 | 外部 | 📋 提案済（手動対応） |
| Google Business Profile | 外部 | 📋 提案済（手動対応） |
| SNSエンティティ構築 | 外部 | 📋 提案済（手動対応） |
| Wikipedia掲載 | 外部 | 📋 提案済（手動対応） |
| 口コミ・レビュー管理 | 外部 | 📋 提案済（手動対応） |
| GA4 AIリファラル計測設定 | 外部 | 📋 提案済（手動対応） |

---

## 参考資料

- [AIO Optimization Best Practices - ResultFirst](https://www.resultfirst.com/blog/ai-seo/aio-optimization-best-practices/)
- [llms.txt Standard](https://llmstxt.org/)
- [noteが最強 AIO対策を徹底解説 - イケハヤ](https://note.com/ihayato/n/n35d8bff0213f)
- [LLMO×AIO対策完全ガイド - トリニアス](https://note.com/trinias/n/n8aeded55e078)
- [Why note.com is strong in Gen AI traffic - VALUES](https://note.com/roberto_saito/n/n0179d5290307)
- [AIO対策の始め方 - クーシー](https://coosy.co.jp/blog/two-aio/)
- [Technical SEO for AI Crawlability - ZipTie.dev](https://ziptie.dev/blog/technical-seo-for-ai-crawlability/)
- [2026 Technical SEO Playbook for AI Crawlers - JetOctopus](https://jetoctopus.com/the-2026-technical-seo-playbook-optimization-for-ai-crawlers-agents/)
