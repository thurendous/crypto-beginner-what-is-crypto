# Slide Design Best Practices

このプレゼンテーション（暗号通貨とは何か？）を編集・追加する際に従うべきデザイン原則。

---

## 1. One Idea Per Slide（1スライド1メッセージ）

- スライド1枚につき**伝えたいことは1つだけ**
- タイトルがそのスライドの「答え」になっていること（疑問形より断言形が強い）
- サブポイントはそのメッセージを支持するものに限る

**悪い例**: 「Bitcoinとは何か＋その歴史＋価格推移」を1枚に詰め込む  
**良い例**: 「Bitcoinは人類初のデジタル希少物だ」という1点に絞る

---

## 2. Visual Hierarchy（視覚的階層）

優先度の順に目が誘導されるよう設計する：

1. **第1レベル**：見出し（h2）— 最大・最太・最高コントラスト
2. **第2レベル**：カードタイトル・強調テキスト — 中サイズ・太字
3. **第3レベル**：本文・説明 — 小サイズ・通常ウェイト
4. **第4レベル**：補足・出典・muted テキスト — 最小・低コントラスト

ルール：**サイズ差・コントラスト差・余白**の3つで階層を表現する。

---

## 3. Information Density（情報密度）

- 箇条書きは **1スライドあたり最大5項目**（理想は3〜4）
- 1項目は **1行〜2行以内**
- カード内の本文は **3〜4文以内**
- グリッドレイアウトは **2×2 または 3列** まで（それ以上は別スライドへ）

> 「削れるものはすべて削る。残ったものが本当に必要なものだ。」

---

## 4. Typography（タイポグラフィ）

このプロジェクトで使用するフォント：
- **見出し**：Space Grotesk（英数字）+ Noto Sans JP（日本語）
- **本文**：Noto Sans JP
- **コード・数値・ラベル**：JetBrains Mono

フォントサイズの基準：
| 用途 | サイズ |
|------|--------|
| スライド見出し (h2) | clamp(32px, 4.2vw, 62px) |
| サブ見出し (h3) | clamp(18px, 2.2vw, 28px) |
| 本文・箇条書き | clamp(16px, 1.9vw, 22px) |
| カードタイトル | 16.5px |
| カード本文 | 15.5px |
| ラベル・タグ | 10〜12px（大文字・letter-spacing） |

---

## 5. Color Usage（色の使い方）

カラーパレット（CSS変数）：
- `--orange` (#f7931a)：Bitcoin関連、強調、CTA
- `--gold` (#fbbf24)：お金・価値の概念、歴史
- `--blue` (#627eea)：Ethereum関連
- `--green` (#00d395)：DeFi・肯定的な概念
- `--purple` (#8b5cf6)：NFT・Web3
- `--red` (#ef4444)：警告・法定通貨の問題・リスク
- `--muted` (#6b7280)：補足情報・弱強調

ルール：
- **1スライドに使う強調色は2色まで**（それ以上は散漫になる）
- 背景グラデーションはそのスライドのテーマ色と一致させる
- テキストは白 (#e8e8f0) か `--muted` のみ（中間色を避ける）

---

## 6. Whitespace（余白）

- スライドの**端から内容まで最低 36px** のパディングを維持
- カード間は **12〜16px** のギャップ
- セクション間（見出し〜本文）は **18〜26px**
- 「余白は空白ではなく、デザインの一部」——詰め込まない

---

## 7. Slide Flow & Narrative（スライドの流れと物語）

このプレゼンが使うナラティブ構造：
1. **問題の設定**（お金とは何か → 法定通貨の問題）
2. **イノベーションの不在**（2600年で数回だけ）
3. **解決への道筋**（サイバーパンク → サトシ → Bitcoin）
4. **証明と普及**（Bitcoin の実績）
5. **次の問いと進化**（Ethereum の必然性）
6. **現在と未来**（DeFi・NFT・エコシステム）

新スライドを追加する際は**このナラティブの中のどこに位置するか**を明確にしてから追加する。

「問いを立てたら、後続のスライドで必ず答えを返す」

---

## 8. Transition Slides（ブリッジスライド）

大きなトピック転換の前に必ずブリッジスライドを入れる：
- 直前のセクションの「まとめ（何が証明されたか）」
- 次のセクションへの「問い（なぜそれが必要か）」

例：Bitcoin → Ethereum の間に「Bitcoinの制約がEthereumを生んだ」スライド。

---

## 9. Component Usage（コンポーネントの使い方）

| コンポーネント | 用途 | 上限 |
|--------------|------|------|
| `.card` | 独立した概念・事実 | 1スライドに4枚まで |
| `.badge` | ラベル・カテゴリ分類 | 1箇所に5つまで |
| `.bullets` | 連続した論点 | 5項目まで |
| `.timeline` / `.tl-item` | 時系列の事実 | 8項目まで |
| `.grid4` (2×2) | 対等な4概念の比較 | 4枚固定 |
| `.step-flow` | プロセス・変遷 | 6ステップまで |

---

## 10. Accessibility & Contrast

- 本文テキストと背景のコントラスト比：**最低 4.5:1**（WCAG AA）
- `--muted` テキストは補足のみに使用（主要情報には使わない）
- フォントサイズは `clamp()` で小画面でも最低サイズを保証する

---

*Sources: [SlideGenius](https://www.slidegenius.com/blog/understanding-visual-hierarchy-in-presentations) · [BrightCarbon](https://www.brightcarbon.com/blog/visual-hierarchy-tips/) · [FlashDocs](https://www.flashdocs.com/post/10-design-principles-every-slide-creator-should-know) · [11FS](https://content.11fs.com/reports/the-10-rules-of-deck-design-for-non-designers) · [Duke LOD](https://sites.duke.edu/lodtraininghub/2025/01/30/create-an-effective-slide-deck/)*
