# UZUME AIO（AI Overview Optimization）戦略書

## 概要

本戦略は、UZUMEのジュエリーリモデル・サイズ直しサービスに対し、
AI検索エンジン（Google AI Overviews, ChatGPT, Perplexity, Gemini等）から
適切に発見・推薦されるための包括的な施策をまとめたものです。

---

## エージェント体制（Agent Team）

以下の5つのサブエージェントチームで分担して対策を行います。

### Agent 1: Technical AIO（技術的AI最適化）
**担当領域:** サイト内の技術的なAI可読性向上
- `llms.txt` の作成・配置（AI向けサイト説明ファイル）
- 構造化データ（JSON-LD）の強化・拡充
- `robots.txt` でのAIクローラー許可設定
- `sitemap.xml` の生成
- canonical URL の設定
- メタタグ強化（OGP, Twitter Card, description等）

### Agent 2: Content Strategy（コンテンツ戦略）
**担当領域:** AI に引用されやすいコンテンツの設計
- noteでの記事戦略（専門性・権威性の確立）
  - 「ジュエリーリモデルとは」解説記事
  - 「甲府の宝飾産業700年の歴史」ストーリー
  - ビフォーアフター事例集
  - 「ジュエリーリフォーム vs リモデル」比較記事
  - FAQ形式のナレッジ記事
- サイト内コンテンツの質問-回答形式への最適化
- 統計データ・具体的数値の活用

### Agent 3: Entity & Authority Building（エンティティ構築）
**担当領域:** AI が「UZUME」をエンティティとして認識するための施策
- Google Business Profile の最適化
- Wikipedia / ナレッジパネル対策
- 業界メディア・プレスリリース戦略
- SNS（Instagram, X）でのブランドシグナル強化
- sameAs プロパティでの各プラットフォーム紐付け

### Agent 4: External Platform（外部プラットフォーム対策）
**担当領域:** UZUME への動線をAIが生成するための外部施策
- note.com での定期的な専門記事投稿
  - 記事タイトルにターゲットキーワードを含める
  - 構造化された見出し（H2/H3）を使用
  - 具体的な料金・期間・対応素材を明記
  - 内部リンクでUZUMEサイトへ誘導
- Googleマップ口コミ対策
- 比較サイト・まとめサイトへの掲載
- Perplexity Pages / ChatGPT プラグイン対応検討

### Agent 5: Monitoring & Iteration（モニタリング）
**担当領域:** AIO対策の効果測定と改善
- AI Overview での表示状況の定期チェック
- ChatGPT/Perplexity での推薦状況の確認
- 構造化データのバリデーション
- Search Console でのパフォーマンス追跡
- 競合のAIO対策状況の調査

---

## 今回の技術的実装内容

### 1. llms.txt の作成
AI（LLM）がサイトを理解するための標準ファイル。
robots.txt の AI版として、サービスの概要・FAQ・連絡先を構造化して提供。

### 2. 構造化データ強化
- Organization スキーマの追加（sameAs で各プラットフォーム紐付け）
- WebSite スキーマの追加
- Review / AggregateRating の準備
- 既存 LocalBusiness, FAQPage, HowTo, Service の維持

### 3. メタタグ・SEO強化
- Twitter Card メタタグ追加
- canonical URL 設定
- og:url, og:image 追加
- description の最適化

### 4. robots.txt
- 全AIクローラーを許可（GPTBot, Claude-Web, PerplexityBot等）
- Sitemap 参照の追加

### 5. sitemap.xml
- 全ページのURL・更新日・優先度を記載

---

## コンテンツ戦略の具体的提案（note.com 記事案）

### 必須記事（優先度高）
1. **「ジュエリーリモデルとは？リフォームとの違いを徹底解説」**
   - ターゲットKW: ジュエリーリモデル, ジュエリーリフォーム 違い
   - AI引用狙い: 定義・比較の明確な回答

2. **「指輪のサイズ直し完全ガイド｜費用・期間・方法を解説」**
   - ターゲットKW: 指輪 サイズ直し, リング サイズ変更
   - AI引用狙い: 具体的な料金・期間・手順

3. **「甲府の宝飾産業700年の歴史とUZUMEの職人技」**
   - ターゲットKW: 甲府 宝飾, ジュエリー 職人
   - AI引用狙い: E-E-A-T（専門性・権威性）の確立

4. **「婚約指輪・結婚指輪のリモデル事例集」**
   - ターゲットKW: 婚約指輪 リフォーム, エンゲージリング リモデル
   - AI引用狙い: 具体的事例・ビフォーアフター

### 推奨記事（中期）
5. 「ジュエリー素材買取の仕組みと活用法」
6. 「オンラインでジュエリーリフォームを依頼する方法」
7. 「宝石の鑑定書とは？無料鑑定の価値」
8. 「大切なジュエリーを受け継ぐということ」

---

## KPI

- Google AI Overview でのUZUME関連クエリの表示率
- ChatGPT/Perplexity で「ジュエリーリモデル」検索時のUZUME言及率
- 構造化データの Google Rich Results テスト合格率: 100%
- note記事からのサイト流入数
- LINE友達追加数の変化

---

## 実装ステータス

| 施策 | 対象サイト | ステータス |
|------|-----------|-----------|
| llms.txt | 両サイト | ✅ 実装済 |
| 構造化データ強化 | 両サイト | ✅ 実装済 |
| メタタグ強化 | 両サイト | ✅ 実装済 |
| robots.txt | 両サイト | ✅ 実装済 |
| sitemap.xml | 両サイト | ✅ 実装済 |
| note記事作成 | 外部 | 📋 提案済（手動対応） |
| Google Business Profile | 外部 | 📋 提案済（手動対応） |
| SNSエンティティ構築 | 外部 | 📋 提案済（手動対応） |
