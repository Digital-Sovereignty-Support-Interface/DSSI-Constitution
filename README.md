# 🏛️ Project DSSI: Digital Sovereignty Support Interface

信頼を製品とする、デジタル主権回復のための仲介レイヤー

---

## 🛠️ Status: Phase 1 - MVP Construction

![DSSI Demo: Password input warning](./images/DSSI_8(chips-counter).png)
![DSSI Demo: Certificate Expiration Warning](./images/DSSI_3(https-cirt-checker).png)
![DSSI Demo: Blocking unsafe submissions](./images/DSSI_6(submit-block).png)
![DSSI Demo: ID input warning](./images/DSSI_4(ID-input).png)
![DSSI Demo: Payment information input warning](./images/DSSI_5(credit-input).png)


**現在、最小機能製品（MVP）の開発フェーズです。**

Phase 1 MVP:

（001）パスワードフィールドにおけるガイド実装：
初期実装（パスワードフィールドの検知とチップス表示：↑**イメージ図**）完了、動作検証済み。

（002）DSSI機能のOn/Offトグル実装

（003）HTTP/HTTPS判定実装・セキュリティ証明書確認（chrome非対応-受動的には取得不可-につき仮実装Phase 2の課題）

送信ボタンへの介入ルール (Submit Guard)

| 条件 | 判定 | 挙動 | 理由 |
| :--- | :--- | :--- | :--- |
| **HTTPS (安全)** | **Pass** | 介入しない（スルー） | ユーザーの意図と安全性が担保されているため。 |
| **HTTP / 証明書エラー** | **Block** | **送信を中断し、確認チップスを表示** | 通信の安全性欠如はユーザーの意図（安全な送信）に反するため。 |
| **非Submit要素** | **Observe** | (検知困難なためPhase 1では対象外) | 入力欄への「キー入力イベント」警告で代替。 |

（004）メールアドレス・クレジット情報への警告実装

（005）保護されていない送信時に再確認表示

（006）チップスの非表示設定（表示回数・非表示スイッチ・非表示リセット・時限復活機能）

**Code Repository:**
[🏛️ DSSI-Code (Implementation)](https://github.com/Digital-Sovereignty-Support-Interface/DSSI-Code)
:実際のソースコード、ビルド手順、技術仕様はこちら。

[🏛️ DSSI System Architecture: DSSIを実装する最小機能コードの概要説明](https://github.com/Digital-Sovereignty-Support-Interface/DSSI-Code/blob/main/docs/ARCHITECTURE.md)

---

## 🌌 Philosophy: 思考を取り戻す

DSSIは、インターネットにおける「情報の非対称性」を解消し、ユーザーが『誰もが自分の責任で生きる』ことを技術的に支援する、憲章駆動型のオープンソースプロジェクトです。

&emsp;&emsp;&emsp;&emsp;&emsp;**私たちは、利便性（自動化）を目的としません。**

&emsp;&emsp;&emsp;&emsp;&emsp;**私たちは、あなたの『思考』を代行しません。**

過度な保護（パターナリズム）は、人を無力にします。

DSSIが目指すのは、ブラックボックス化された技術をただ使うのではなく、「**使う過程で分かるようになる（教育）**」構造の実装です。

私たちは自動化・省力化ではなく、技術的な**情報**と**知識**を提供することで、ユーザーがデジタルシーンにおける「**主権**者」としての「**判断**」能力を回復することを目的とします。

---

### Three Principles

1. **勝手に入力しない**（非自動化）
2. **事実を隠さない**（透明化）
3. **防御を支援する**（支援原則）

---

### 🛡️ Stance: The Aesthetics of Observation (観測の美学)

DSSIは、サイト側の解析拒否や妨害に対して、技術的な突破（ハッキング）を試みません。

私たちは、解析を拒む実装を**悪**として戦うのではなく、「DSSI技術よりも**不透明である」という事実**のみを提示し、その**実装技術を鑑賞する**立場を貫きます。

深入りせず、こじ開けず、ただ**扉が閉じられている**（**錠をあけなかった**）ことをユーザーに告げる。
それが、私たちが定義する**アンタッチャブル**（深入り抑止）の作法です。

---

## 🧭 Core Documents (rMass)

本プロジェクトは、以下の文書群（カーネル）によって厳格に統制されています。

| Document | Description |
| :--- | :--- |
| 📜 **[DSSI 倫理憲章](./DSSI_Constitution.md)** | プロジェクトの最上位法規。開発における絶対的な倫理基準。 |
| 🗺️ **[戦略設計図](./DSSI_Strategic_Blueprint.md)** | 開発ロードマップ、対敵対的防御構造、ビジネスモデル。 |
| 🧠 **[哲学的アーキテクチャ](./DSSI_Philosophical_Architecture.md)** | 「熱力学」「愛と恋のプロトコル」に基づく理論的基盤。 |
| 🌱 **[創発記録](./DSSI_Genesis_Log.md)** | 本プロジェクトの根源的な問いと、創発の記録。 |

---

## 📦 Official Repositories

DSSIプロジェクトは、機能ごとに以下のリポジトリで構成されています。

| Repository | Role | Description |
| :--- | :--- | :--- |
| **[DSSI-Constitution](./)** | **Side-i (理念)** | 憲章、戦略設計図、創発ログの格納場所。（本リポジトリ） |
| **[DSSI-Code](https://github.com/Digital-Sovereignty-Support-Interface/DSSI-Code)** | **Side-r (実装)** | ブラウザ拡張機能のソースコード、技術仕様書。 |

## 🤝 Contribution

貢献を歓迎します。ただし、私たちと共に「**倫理的純度**」という名の最大の防御壁を築く意志を持つ同志のみ。

コードを提出する前に、必ず以下の作法に従ってください。

**[貢献ガイドライン (CONTRIBUTING)](./CONTRIBUTING.md)**

>&emsp; *「コードのプルリクエストは、**哲学のプルリクエスト**である。」*

---

コア哲学：
**正しい判断は過不足ない判断材料から**

&emsp;&emsp;&emsp;*「知識の本質を開示し、技術的な真実を共有する」*

&emsp;&emsp;&emsp;*「自動化や省力化などの利便性よりも、自律的な判断の強化を優先する」*

**この種子が芽吹くその時まで、私たちは静かに耕し続けます。**
