# social-case-to-excel

Turn social posts into traceable case libraries, method breakdowns and illustrated research documents.

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

## What we use it for

We have used this workflow to reconstruct brands’ early overseas activity, organize social marketing cases and analyze customer needs in comments. Each case covers the action, available outcome evidence, execution steps and what other brands can adapt.

Hardware brands are one research sample. Topics can also include AI advertising, product launches, cross-border commerce and content operations.

| Deliverable | Contents |
| --- | --- |
| Excel case library | Actors, actions, reported outcomes, dates, source links, categories and evidence limits |
| Method breakdown | Steps, prerequisites and adaptations for different brands |
| Images and screenshots | Matched post images, video covers or screenshots with captions and source references |
| Research document | Findings, cases and methods in readable Markdown; HTML when requested |
| Candidate records | Search scope and rejected candidates for review and follow-up work |

## Ways to use it: from examples to business decisions

Start with a business question, then turn public records into evidence, methods and options.

| Use case | Research task | What it helps you do |
| --- | --- | --- |
| B2B acquisition | Study channel activity, content, community participation and reported outcomes | Build a case library and plan channel/content experiments |
| Brand and overseas launch research | Reconstruct early activity across official accounts, users, media and moderators | Create timelines and learn launch methods |
| AI creative advertising | Analyze image/video concepts, AI techniques and production evidence | Build creative references and adaptable prompt drafts; inferred prompts are not original creator prompts |
| Market and product research | Identify users, jobs, obstacles and desired features | Map scenarios and prepare validation questions |
| Competitor analysis | Compare positioning, functions, bundles and services | Develop evidence-based differentiation hypotheses |
| Reviews and negative feedback | Read actual praise, complaints and usage barriers | Improve products, FAQs and content; a small sample is not market share |
| Reddit communities | Examine discussions, rules, needs and promotional content | Plan useful community participation without fake testimonials or bulk posting |
| Public-sector social listening | Track public policies, service feedback and open discussions | Produce neutral issue summaries and timelines; online activity is not a public-opinion poll |
| 1688 sourcing | Compare suppliers, kits, SKUs, minimum orders and tier prices | Prepare procurement candidates and verification questions; listings do not certify quality or authorization |
| Cross-marketplace pricing | Compare 1688, Amazon, Temu and Walmart by model, pack size and included functions | Study productization without treating price differences as profit |

Commerce, sourcing and public-issue studies are adaptable workflows, **not bundled one-click features**. Use the ClaudeBaby tools actually exposed by the host, verify fields and report missing coverage. Adapt the output schema to the task.

## What we have used this workflow for

| Study | Intent | Goal supported |
| --- | --- | --- |
| Chinese brands' first overseas year, especially X and Reddit | Find early actions and non-official discussion | Learn launch and community methods |
| B2B social acquisition | Understand trust-building and inquiry generation | Design channel experiments |
| Independent sites, SEO/GEO and Reddit, excluding pure promotional posts | Find practices with processes and evidence | Choose search, content and community approaches |
| AI creative ads | Learn concepts and methods for other brands | Prepare creative references and production plans, not claim campaign results |
| ESP32 with agents/AI | Find useful, reproducible hardware scenarios | Inform AuraBaba integration, demo content and acquisition plans |
| ESP32 sourcing and overseas product comparisons | Check low-cost parts, complete kits and actual SKUs | Prepare procurement and productization options, not claim purchases, manufacturing or profit |

The sequence is: **find examples → analyze methods → identify users and needs → design experiments → choose sourcing and content paths**. Development, publishing, purchasing and conversion still require separate execution and validation.

## Example requests

- “Research B2B acquisition cases in our industry, with methods, outcome evidence, audience fit and an illustrated workbook.”
- “Read actual competitor reviews and complaints; retain source text and distinguish needs from your recommendations.”
- “Query complete 1688 development kits through ClaudeBaby; verify SKUs, minimum orders, included parts and prices.”
- “Compare domestic sourcing and overseas offers by model and pack size, separating facts, hypotheses and advice.”
- “Neutrally summarize a public institution's policies, service feedback and discussion over a defined time window.”

## Example: the first year of Chinese brands overseas

One historical study organized 44 events across OnePlus, Anker, Bambu Lab, Keychron, Snapmaker and EcoFlow. It separated pre-launch activity, first-year records and other early clues, and included official accounts, media, community moderators and users.

OnePlus records show contact with moderators and executive Q&A. A Keychron post describes buying through crowdfunding before sharing on Reddit. Bambu Lab discussions include questions about demonstrations, materials and delivery. These are method references, not proof that social engagement or crowdfunding totals equal channel-attributed sales.

The following are excerpts from an actual workbook. The sample screenshots remain in Chinese in all language editions. Historical sample coverage does not guarantee the same platform permissions in a current connection.

### Method breakdown

![Method breakdown sample](assets/readme/methods.png)

### Brand adaptations

![Brand reference sample](assets/readme/brand-reference.png)

### Timeline and outcome evidence

![Timeline sample](assets/readme/timeline.png)

Excel samples belong in [`outputs/`](outputs/); each file is introduced by its actual research topic.

## Usage

Install this folder in your Agent’s supported skills directory. Invoke `$social-case-to-excel` with a topic, platforms, date range and desired number of cases. For example:

> Reconstruct the early overseas history of several Chinese brands using X and Reddit. Include official, media and user records, methods, outcome evidence and adaptations by category. Produce an illustrated Excel workbook and research document.

Python workbook generation requires `openpyxl` and `Pillow`. Scripts are templates to adapt for each study. For other platforms, use the ClaudeBaby tools exposed by the host connection.

## Data connection

This version uses **ClaudeBaby** as its sole data service. Reddit, X, YouTube and Bilibili are target platforms; available tools and permissions determine coverage.

At first use, check the existing ClaudeBaby MCP connection and target-platform capabilities. Guide registration and setup only if needed.

```bash
python3 scripts/claudebaby_preflight.py          # Offline configuration check
python3 scripts/claudebaby_preflight.py --probe  # MCP handshake and tool discovery
```

The HTTP client reads `CLAUDEBABY_MCP_URL` and `CLAUDEBABY_MCP_TOKEN`, with legacy `REDDIT_MCP_*` support. Use the endpoint and authentication information from the console; never put tokens in reports or the repository.

Reports preserve source links, dates and evidence limits. Reported results are distinguished from research inferences; a cover image does not establish that the full video was reviewed. Source media rights remain with their owners; check permitted use before republication.

## ClaudeBaby and this project

[Register with the ClaudeBaby invitation link](https://claudebaby.cn/console/register?ref=M8YYGRN4) · Invitation code: `M8YYGRN4`. Registration through this link provides invitation credits. Existing users can keep their current connection.

If this skill or its samples help your research, you are welcome to ⭐ Star this repository.

```text
social-case-to-excel/
├── SKILL.md
├── README.md / README.en.md / README.ja.md / README.ko.md
├── assets/readme/
├── outputs/
├── references/
└── scripts/
```

## Installation / 安装 / インストール / 설치

```bash
npx skills add lingling1989r/social-case-to-excel --skill social-case-to-excel
```

[GitHub](https://github.com/lingling1989r/social-case-to-excel) · [ZIP](https://github.com/lingling1989r/social-case-to-excel/archive/refs/heads/main.zip)

