# Privacy Label Initiative

> **データ主権を取り戻す。すべての人が、自分のデータを自分でコントロールできる社会へ。**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Code of Conduct](https://img.shields.io/badge/Code%20of-Conduct-blue.svg)](CODE_OF_CONDUCT.md)

---

## 🚨 プロジェクトからの緊急募集

**【運営リーダー募集中】** 本プロジェクトを一緒に運営してくれるリーダーを募集しています。

👉 **[CALL_FOR_LEADERS.md](CALL_FOR_LEADERS.md) をお読みください**

応募締切: **2025年11月30日**

---

## 📋 目次

- [私たちのビジョン](#私たちのビジョン)
- [データ主権ラベルとは](#データ主権ラベルとは)
- [なぜ今なのか](#なぜ今なのか)
- [私たちが作るもの](#私たちが作るもの)
- [参加方法](#参加方法)
- [ロードマップ](#ロードマップ)
- [プロジェクト体制](#プロジェクト体制)
- [リソース](#リソース)

---

## 🎯 私たちのビジョン

**すべての人が、自分のデータを自分でコントロールできる社会を実現する。**

IoTデバイスが家庭に溢れる時代、私たちは知らないうちに監視され、データを搾取されています。

- 🎤 **音声が無断で録音**され、外国のサーバーに送信
- 📹 **映像が収集**され、誰が見ているか不明
- 📍 **生活パターンが記録**され、プロファイリング
- 🌍 データは**中国など権威主義国家**に送信
- ⚠️ **中国政府が法的にアクセス可能**（国家情報法）

**しかも、消費者は購入前にこれを知ることができません。**

私たちは、**データ主権ラベル**制度を提案し、実装し、法制化することで、この状況を変えます。

詳細は [MANIFESTO.md](MANIFESTO.md) をお読みください。

---

## 🏷️ データ主権ラベルとは

タバコの警告表示や食品のアレルゲン表示と同様に、**IoTデバイスにプライバシーリスクを表示**する制度です。

### 表示内容

```
┌─────────────────────────────────┐
│  🔴 データ主権リスク: 高         │
│                                 │
│  このデバイスは以下を収集・送信: │
│  🎤 音声データ                   │
│  📊 視聴履歴・生活パターン       │
│                                 │
│  送信先: 🇨🇳 中華人民共和国       │
│                                 │
│  ⚠️ 中国政府がアクセス可能       │
│  ⚠️ 削除保証なし                │
│                                 │
│  詳細 → [QRコード]              │
└─────────────────────────────────┘
```

### リスクレベル

- 🔴 **高リスク**: 権威主義国家へ送信、政府の無令状アクセス可能
- 🟡 **中リスク**: 民主主義国へ送信、司法統制あり
- 🟢 **低リスク**: 日本国内のみ、削除保証あり

### 技術仕様

機械可読なJSON形式で、製品のプライバシー情報を標準化:

```json
{
  "version": "1.0",
  "product": {
    "name": "Example Smart Speaker",
    "manufacturer": "Example Corp"
  },
  "privacy": {
    "risk_level": "high",
    "data_collection": ["voice", "usage_history"],
    "data_destination": ["CN", "US"],
    "government_access": {
      "country": "CN",
      "legal_basis": "National Intelligence Law"
    }
  }
}
```

---

## ⏰ なぜ今なのか

### 🏛️ 政治的好機

**高市政権**が発足し、経済安全保障とサイバーセキュリティが国家戦略の中核に。

- 経済安全保障推進法の本格運用
- サイバーセキュリティ基本法の改正検討
- AI基本法の制定議論
- デジタル庁の体制強化
- **2026年通常国会で法案提出の好機**

### 🌍 国際的潮流

- **EU**: GDPR、デジタルサービス法、AI規制法
- **米国**: FCC IoT Security Label（パイロット開始）
- **豪州**: 重要インフラ法、中国企業排除

日本も遅れを取ってはいけません。

### 💡 技術的成熟

- JSON Schemaで標準化可能
- オープンソースツールで実装可能
- 既存の印刷・WEB技術で表示可能

**技術的にも、政治的にも、今が千歳一遇のチャンスです。**

---

## 🛠️ 私たちが作るもの

### Phase 1: 基盤構築（2025年11-12月）

#### 📐 [json-schema](https://github.com/privacy-label-initiative/json-schema)
機械可読なラベル情報の標準形式

#### 🔧 [generator-python](https://github.com/privacy-label-initiative/generator-python)
企業が簡単にラベルを生成できるPythonツール

#### 📚 [docs](https://github.com/privacy-label-initiative/docs)
実装ガイド、ベストプラクティス

### Phase 2: 検証ツール（2026年1-3月）

#### 🔍 [traffic-monitor](https://github.com/privacy-label-initiative/traffic-monitor)
デバイスが実際に何を送信しているか可視化

#### 🔬 [firmware-analyzer](https://github.com/privacy-label-initiative/firmware-analyzer)
ファームウェアの静的解析、バックドア検出

#### 📊 [verification-report](https://github.com/privacy-label-initiative/verification-report)
検証レポート生成、消費者庁への通報機能

### Phase 3: 消費者向けツール（2026年4-6月）

#### 🌐 [browser-extension](https://github.com/privacy-label-initiative/browser-extension)
ECサイトで自動的にラベル表示

#### 📱 [mobile-app](https://github.com/privacy-label-initiative/mobile-app)
製品バーコードスキャンでラベル表示

#### 🏆 [comparison-site](https://github.com/privacy-label-initiative/comparison-site)
製品のプライバシースコアをランキング

### Phase 4: 政策支援（2026年通年）

#### ⚖️ [policy](https://github.com/privacy-label-initiative/policy)
法案骨子、パブリックコメント、国際標準化提案

---

## 🤝 参加方法

### あなたができること

| 役割 | 貢献内容 | 始め方 |
|------|---------|--------|
| 🖥️ **開発者** | コードを書く、レビュー、バグ修正 | [CONTRIBUTING.md](CONTRIBUTING.md) |
| 🎨 **デザイナー** | ラベルデザイン、UI/UX、図解 | [Design Guidelines](design/) |
| ✍️ **ライター** | ドキュメント、ブログ、翻訳 | [Writing Guide](docs/writing-guide.md) |
| ⚖️ **法律家** | 法令調査、法案起案、コンプライアンス | [Legal Team](legal/) |
| 🔬 **研究者** | 論文執筆、実証研究、標準化 | [Research](research/) |
| 📢 **広報** | SNS、メディア対応、イベント企画 | [Communications](communications/) |
| 🌐 **翻訳者** | 英語・他言語への翻訳 | [Translation Guide](docs/translation-guide.md) |
| 👥 **一般市民** | SNS拡散、署名、議員への働きかけ | [Activism Guide](activism/) |

### 運営リーダーに応募する

**📣 [CALL_FOR_LEADERS.md](CALL_FOR_LEADERS.md) をお読みください**

---

## 🗓️ ロードマップ

```
2025年11月
├─ ✅ プロジェクト立ち上げ
├─ 🔄 運営リーダー募集・選定
└─ 🔄 初期チームの形成

2025年12月
├─ JSON Schema v1.0 確定
├─ ラベル生成ツール開発開始
└─ 政府（デジタル庁）への初回説明

2026年1-3月
├─ パイロット実装（協力企業募集）
├─ 政府へのデモ・実証実験
└─ 法案骨子の技術的サポート

2026年4-6月
├─ 通常国会での法案審議
├─ パブリックコメント対応
└─ メディア露出の拡大

2026年夏
├─ 自主採用企業の登場
├─ ツールのv1.0リリース
└─ 国際標準化提案（ISO/IEC JTC 1）

2027年
├─ 法制化
├─ 段階的義務化開始
└─ グローバル展開

2030年
├─ 完全施行
├─ 国際標準として確立
└─ データ主権保護が当たり前の社会へ
```

---

## 👥 プロジェクト体制

### 発起人（Founder/Sponsor）
経営者（Qiita記事著者）。政治・産業界との橋渡し役。

### 運営委員会（Steering Committee）
選出された3-5名の運営リーダー。日常運営と方向性決定。
**📣 現在募集中 → [CALL_FOR_LEADERS.md](CALL_FOR_LEADERS.md)**

### 助言委員会（Advisory Board）
発起人、学識経験者、業界専門家。戦略的助言。

### 技術委員会（Technical Committee）
コントリビューターから選出。技術仕様の決定。

### コントリビューター
すべての参加者。あなたもここに含まれます。

---

## 📚 リソース

### 📖 ドキュメント
- [MANIFESTO.md](MANIFESTO.md) - プロジェクト宣言
- [CONTRIBUTING.md](CONTRIBUTING.md) - 貢献ガイド
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - 行動規範
- [GOVERNANCE.md](GOVERNANCE.md) - ガバナンス構造（準備中）

### 📰 メディア
- [Qiita記事](リンク) - プロジェクトの背景と提案
- [プレスキット](press-kit/) - メディア向け資料
- [FAQ](FAQ.md) - よくある質問

### 🔗 外部リンク
- [公式サイト](https://privacy-label.org)（準備中）
- [Twitter](https://twitter.com/PrivacyLabelJP)（準備中）
- [署名サイト](Change.orgリンク)（準備中）

### 📧 連絡先
- **一般的な質問**: [GitHub Discussions](https://github.com/orgs/privacy-label-initiative/discussions)
- **運営リーダー応募**: [Issue #1](https://github.com/privacy-label-initiative/manifesto/issues/1)
- **メディア取材**: media@privacy-label.org（準備中）
- **政府・企業**: official@privacy-label.org（準備中）

---

## ⚖️ ライセンス

### コード
- **MITライセンス** （一部はApache 2.0）
- 商用利用、改変、再配布すべて自由

### ドキュメント
- **CC BY 4.0** （クリエイティブ・コモンズ 表示 4.0 国際）
- 出典を明記すれば自由に利用可能

### ラベルデザイン
- **CC0**（パブリックドメイン）
- 誰でも、許可なく、自由に使用可能

---

## 🌟 スポンサー

本プロジェクトは、現在スポンサーを受け付けていません。  
将来的に財団化した際に、透明性のある形でスポンサーシップを検討します。

---

## 🙏 謝辞

このプロジェクトは、以下の方々・組織の協力により成り立っています:

- 発起人（Qiita記事著者）
- すべてのコントリビューター
- （今後、協力企業・団体を追加）

---

## 📢 最新情報

### お知らせ

**【2025年11月】プロジェクト立ち上げ**
- GitHub Organization設立
- 運営リーダー募集開始
- 初期ドキュメント公開

### SNSで最新情報をフォロー

- Twitter: [@PrivacyLabelJP](https://twitter.com/PrivacyLabelJP)（準備中）
- Mastodon: @privacy-label@mastodon.social（検討中）

### ニュースレター

月1回、プロジェクトの進捗をメールでお届けします。  
（準備中）

---

## 💬 コミュニティ

### 議論の場

- **GitHub Discussions**: 技術的議論、アイデア提案
- **Slack** (準備中): 日常的なコミュニケーション
- **Discord** (検討中): リアルタイムチャット

### イベント

- **定例ミーティング**: 月2回、オンライン（運営チーム選定後開始）
- **技術カンファレンス**: PyCon JP、RubyKaigi等でトーク予定
- **勉強会**: 全国各地で開催（協力者募集）

---

## ❓ FAQ

### Q: このプロジェクトは誰が運営していますか？
A: 発起人（経営者）が立ち上げましたが、日常運営はコミュニティ主導です。現在、運営リーダーを募集中です。

### Q: 参加に費用はかかりますか？
A: 完全無料です。オープンソースプロジェクトです。

### Q: 技術的に初心者ですが参加できますか？
A: もちろんです。開発以外にも、ドキュメント、デザイン、翻訳、広報など多様な貢献方法があります。

### Q: 企業として協力したいのですが？
A: 大歓迎です。[GitHub Discussions](https://github.com/orgs/privacy-label-initiative/discussions)で提案してください。

詳しくは [FAQ.md](FAQ.md) をご覧ください。

---

## 🚀 今すぐ始める

1. **⭐ このOrganizationをStar**
2. **👀 [MANIFESTO.md](MANIFESTO.md) を読む**
3. **💬 [GitHub Discussions](https://github.com/orgs/privacy-label-initiative/discussions)に参加**
4. **🛠️ [CONTRIBUTING.md](CONTRIBUTING.md)を読んで、最初の貢献をする**
5. **📢 SNSでシェア** (#データ主権ラベル)

---

## 🎯 スローガン

**"Know Your Data, Own Your Future"**

**「自分のデータを知り、自分の未来を創る」**

---

<div align="center">

**一緒に、未来を変えましょう。**

[運営リーダーに応募する](CALL_FOR_LEADERS.md) | [貢献する](CONTRIBUTING.md) | [議論に参加](https://github.com/orgs/privacy-label-initiative/discussions)

---

Made with ❤️ by Privacy Label Initiative Community

</div>
