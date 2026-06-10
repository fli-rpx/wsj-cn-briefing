# 华尔街日报每日简报 — 2026年6月10日 中文版

## Project
Build a single self-contained HTML page that is a Chinese-language version of the WSJ Daily Briefing page at https://fli-rpx.github.io/news_briefing/briefings/wsj_2026-06-10.html

Output: `/Users/fudongli/Projects/wsj-cn-briefing/index.html`

## Design Requirements

### Layout Structure (exact match with the English version)

1. **Header bar** — Dark navy/black background. Left side: "WSJ" logo (no link), next to it "每日简报" (Daily Briefing). Right side: minimal.

2. **Navigation** — Sticky horizontal nav bar below header with section buttons:
   - 摘要 (SUMMARY)
   - 市场 (MARKETS)
   - 经济 (ECONOMY)
   - 地缘政治 (GEOPOLITICS)
   - 行业 (SECTOR)
   - 展望 (OUTLOOK)
   - 评论 (OBSERVER)
   - 漫画 (CARTOON)

   Each button scrolls smoothly to the corresponding section. Active/highlighted state on scroll.

3. **Hero section** — Centered text:
   - "华尔街日报 — 每日简报" in large bold text
   - Date: "2026年6月10日"
   - Reading time: "阅读约需7分钟"

4. **Today's Top Stories** — 7 clickable story cards in a grid (2 columns on desktop, 1 on mobile). Each card has a number badge, headline, and brief tag. Cards have hover effect.

5. **"阅读简报" (READ BRIEFING) button** — Centered CTA below the cards.

6. **Executive Summary section** — Title "执行摘要" with the main narrative paragraph in Chinese.

7. **MARKETS section** — Title "市场 · CPI冲击波蔓延全球市场". Sub-sections with:
   - CPI inflation data
   - European Indices table (7 rows: FTSE 100, DAX, CAC 40, FTSE MIB, IBEX 35, STOXX 600, Euro Stoxx 50 with change %)
   - Market analysis

8. **ECONOMY section** — Title "经济 · 通胀、退休与工资底线"
   - Sub-sections with analysis

9. **GEOPOLITICS section** — Title "地缘政治 · 没有出路"
   - US-Iran escalation
   - Taiwan HIMARS test
   - North Korea enrichment
   - UK anti-migrant violence

10. **SECTOR section** — Title "行业 · AI军备竞赛遇上创纪录IPO"
    - Anthropic Claude Fable 5
    - SpaceX $75B IPO
    - NextEra-PGE merger

11. **OUTLOOK section** — Title "展望 · 概率加权前景" with a clean Probability-Weighted Outlook table:
    | 情景 (Scenario) | 概率 (Probability) | 时间 (Horizon) |
    |---|---|---|
    | 美伊冲突升级 | 55% | 30天 |
    | 美伊停火 | 20% | 30天 |
    | SpaceX首周上涨 | 70% | 7天 |
    | SpaceX跌破首日价 | 40% | 90天 |
    | 中国对台无回应 | 85% | 90天 |
    | 朝鲜政策回应 | 30% | 6个月 |
    | 美伊无出路 | 65% | 30天 |

    Each row has a visual progress bar showing the probability.

12. **OBSERVER section** — Title "三重视角 · 全球失序" with three cards:
    - **翟东升** (体系/结构视角) — commentary text
    - **金灿荣** (美国政治/战略相持视角) — commentary text
    - **宋鸿兵** (货币/债务/周期视角) — commentary text with quote "4.2%的CPI数据不仅仅是通胀——它是美元体系矛盾的可见症状。美联储面临滞胀陷阱:每一次利率决策现在都在损害增长或信誉。"

13. **CARTOON section** — Title "每日一图" with a placeholder area for the daily cartoon.

14. **Footer** — "The Briefing in One Frame" section and a small "由Kimi驱动" (Powered by Kimi) credit.

### Content (Chinese versions of the WSJ June 10 briefing)

Use the following content (translated and adapted from the English briefing):

**Executive Summary:**
美国5月CPI同比上涨4.2%，创2023年4月以来新高，伊朗能源冲击波及全球供应链。华盛顿与德黑兰进入危险新阶段——伊朗沙赫德无人机击落美军阿帕奇直升机，机组人员在海上漂流两小时后获救。特朗普威胁打击伊朗电厂和桥梁。SpaceX周五启动史上最大IPO（750亿美元），Anthropic向公众发布Claude Fable 5"神话级"AI模型。朝鲜铀浓缩能力可能扩大75%，台湾首次向大陆方向试射32枚HIMARS火箭，北爱尔兰反移民骚乱再次爆发。

**Market Data - European Indices:**
FTSE 100: +0.13% | DAX: -0.03% | CAC 40: +0.25% | FTSE MIB: +0.89% | IBEX 35: +0.46% | STOXX 600: +0.11% | Euro Stoxx 50: +0.08%

**Key stories to include:**
1. US-Iran escalation: 3 days of clashes, Apache helicopter downed by Shahed drone, Trump threatens power plants
2. Taiwan HIMARS test: 32 test rockets fired toward China, calibrated signaling
3. North Korea: uranium enrichment could expand 75%, Kim visited "mammoth facility"
4. UK anti-migrant violence: Belfast second flare-up, Sudanese asylum seeker charged
5. CPI 4.2%: highest since April 2023, driven by Iran energy costs
6. SpaceX IPO: $75 billion record listing Friday
7. Anthropic Fable 5: "Mythos-class" AI with constitutional guardrails
8. NextEra-PGE merger
9. World Cup/other stories

### Visual Design

- **Dark theme**: Background #0a0a0f, cards #141420, text #e0e0e0
- **Accent colors**: Gold/amber (#d4a853) for highlights, red (#e74c3c) for critical risk tags, green (#2ecc71) for positive market moves
- **Typography**: System fonts (-apple-system, PingFang SC, Microsoft YaHei, sans-serif)
- **Responsive**: Full desktop width (1200px max), mobile-friendly with stacked layout
- **Smooth scroll** between sections
- **Sticky nav** that highlights the current section
- **Cards** with subtle borders, rounded corners, hover shadow effects
- **Probability bars** in the outlook table (colored by percentage)
- **Risk badges** like "风险等级: 严重" with colored indicators
- All interactive via JavaScript (no external dependencies — pure HTML/CSS/JS)

### File Structure
Only ONE file: `/Users/fudongli/Projects/wsj-cn-briefing/index.html`
Self-contained: all CSS inline in `<style>`, all JS inline in `<script>`.
No external assets (no CDN fonts, no external images).
