# PREZIP — Warm Precision Design System

PREZIP의 디자인은 **따뜻한 공간 감성**과 **명확한 의사결정 도구**의 결합이다. 예쁜 집을 전시하는 콘텐츠 플랫폼보다, 고객이 공사 전에 충분히 이해하고 비교하고 승인할 수 있게 하는 제품이어야 한다.

## 1. Visual Theme & Atmosphere

**Warm Precision.** White와 아주 옅은 Warm Gray를 넓게 사용하고, Forest Green은 중요한 결정과 진행 상태에만 쓴다. Oak는 자재와 생활 감성을 연결하는 보조색이다. 전체 인상은 차분하고 정돈되어야 하며, 차가운 테크 SaaS나 과도하게 감성적인 인테리어 매거진처럼 보이면 안 된다.

Mood: clear, reassuring, warm, structured, trustworthy.

핵심 대비:

- 생활 이미지와 온기 → White, Oak, 부드러운 라운드
- 계약과 비용의 정확성 → 얇은 선, 정렬된 숫자, 표준화된 표
- 진행의 연결성 → ZIP LINE, 단계 표시, 버전 이력

## 2. Brand Principles

1. **Show before Tell** — 설명보다 시안, 적용 자재, 예상비용을 먼저 보여준다.
2. **Same Condition** — 업체 비교는 반드시 같은 열과 같은 기준을 쓴다.
3. **Everything Leaves a Record** — 견적, 계약, 변경, 승인, 공정, A/S는 버전과 상태를 남긴다.
4. **Easy First** — 전문 용어를 생활 언어로 풀고, 한 화면에는 하나의 중요한 결정을 둔다.
5. **Green means decision** — 초록색은 브랜드 장식이 아니라 선택, 완료, 진행, 승인에 쓴다.

## 3. Color Palette & Roles

```css
--pz-white: #FFFFFF;
--pz-canvas: #F7F7F3;
--pz-surface-soft: #F1F2EC;
--pz-forest-700: #31563C;
--pz-forest-600: #3E6B4A;
--pz-forest-100: #E4EEE5;
--pz-sage-500: #7FA87A;
--pz-sage-100: #EDF4EC;
--pz-oak-500: #B8865E;
--pz-oak-100: #F4E9DE;
--pz-charcoal: #202420;
--pz-text-secondary: #5E655E;
--pz-text-muted: #858C85;
--pz-line: #DDE1DA;
--pz-line-strong: #C7CEC5;
--pz-info: #416C86;
--pz-warning: #9A672E;
--pz-danger: #A3453F;
```

Rules:

- Canvas의 80% 이상은 White 또는 Warm Neutral로 유지한다.
- Forest Green은 Primary CTA, active step, approved status, positive delta에만 쓴다.
- Oak는 자재, 공간, 선택의 온도를 높이는 작은 보조 표시에 쓴다.
- 경고·위험 상태에 초록색을 사용하지 않는다.
- 표와 숫자는 색보다 정렬, 굵기, 기호로 먼저 구분한다.

## 4. Typography Rules

- Korean UI / body: `Pretendard Variable`, `Pretendard`, `Noto Sans KR`, system sans.
- English / numerals: `Inter`, system sans. 가격과 일정에는 tabular numerals를 적용한다.
- Display: 동일 sans 계열의 600–700 weight. 브랜드가 확정되기 전 별도 serif를 도입하지 않는다.
- Mono: `SFMono-Regular`, `Consolas` — 토큰명, 프로젝트 ID, 견적 버전에만 사용한다.

Type scale:

`14 / 15 / 16 / 18 / 20 / 24 / 32 / 40 / 52 / 72`

- Display 72/76, 700, letter-spacing -0.045em
- H1 52/60, 700, letter-spacing -0.035em
- H2 40/48, 700, letter-spacing -0.025em
- H3 32/40, 650
- Title 24/34, 650
- Body 18/29, 400
- UI 16/23, 550
- Caption 14/21, 500
- Dense comparison metadata may use 12–13px only when it is supplementary and never interactive.

## 5. Spacing & Layout

- Base unit: 4px
- Scale: 4 / 8 / 12 / 16 / 20 / 24 / 32 / 40 / 48 / 64 / 80 / 96
- App shell max width: 1440px
- Reading width: 720px
- Content grid: 12 columns, desktop gutter 24px
- Desktop page padding: 40px; tablet 24px; mobile 16px
- Section gap: 80px desktop, 56px mobile
- Form width: 680px; comparison tables may use the full content width

## 6. Shape, Border & Depth

- Radius: 6px controls, 10px inputs, 14px cards, 20px feature surfaces
- Border: 1px solid `--pz-line`
- Default cards remain flat. Use shadows only for floating menus, modals, and selected decision surfaces.
- Selected card: Forest border plus a subtle green ring; never scale on hover.
- Use hairlines and surface shifts before adding shadows.

## 7. Signature Motifs

### ZIP LINE

A thin connecting line with square “teeth” or nodes. Use for onboarding, project steps, contract version history, and construction progress. It represents disconnected decisions becoming one project record.

### HOME FRAME

An open rectangular frame, not a filled house icon. Use sparingly in empty states or brand moments.

### BEFORE / AFTER SPLIT

Place the current condition and the decided outcome side-by-side with a single vertical ZIP line. Never use it as a decorative wipe on every page.

## 8. Component Styling

### Buttons

- Primary: Forest 600 fill, white label, radius 8, height 48–52. Hover Forest 700.
- Secondary: white fill, strong line, charcoal label.
- Tertiary: transparent, charcoal label; underline or soft surface on hover.
- Destructive: danger text or danger fill only inside explicit confirmation flows.
- Icon-only buttons require a visible tooltip and 44px touch target.

### Inputs

- White background, 1px line, radius 10, min-height 48.
- Focus: 2px Forest ring with 2px offset.
- Label sits above; helper/error text below. Placeholder never replaces a label.
- Cost input aligns numerals right and keeps the currency outside the editable value.

### Cards

- Use cards only for selectable objects or meaningful grouped records.
- Material card: photo/texture area, material name, performance, price band, selection state.
- Contractor card: name, verification, fit, price, duration, A/S; use the same order for all vendors.
- Approval card: changed item, reason, cost delta, schedule delta, primary decision actions.
- TODAY'S ZIP: date, progress, photos, changes, extra cost, next work.

### Tables

- Sticky first column where useful; tabular numerals; price right-aligned.
- Same-condition rows appear first. Differences use text labels and a light surface, not color alone.
- On mobile, comparison tables become vendor-switched key-value cards. Do not squeeze all columns.

### Status

- Draft: neutral gray
- In progress: sage
- Approval needed: oak/warning
- Approved/completed: forest
- Issue/overdue: danger
- Every status includes text, not color alone.

## 9. Core Screen Patterns

### Project setup

One decision group per step. Show completion, skipped items, and recommendation reasons. Keep the running budget visible but secondary.

### AI preview

The image is the hero, but always pair it with applied conditions and a disclaimer. Provide “keep” and “change” actions rather than a blank prompt as the primary interaction.

### Standard estimate

Lead with the total range, confidence, included scope, and top three cost drivers. Detailed rows follow. Visually distinguish preliminary, proposal, and final versions.

### Contractor comparison

Same columns, same item order, and a clear “conditions differ” state. Do not rank solely by price. Keep selection persistent while the user inspects details.

### Construction tracking

Show today first: current trade, percentage, photos, changes, extra cost, and next step. Historical records follow as a timeline.

### Change approval

Show before/after conditions, reason, cost impact, schedule impact, and attachments before the buttons. Approval is the only green primary action.

## 10. Motion

- Duration: 120ms feedback, 180ms component transition, 280ms panel transition.
- Easing: `cubic-bezier(.2,.8,.2,1)`.
- The ZIP LINE may fill from left to right when progress changes.
- Never use bouncing, floating cards, parallax, or decorative infinite motion.
- Respect `prefers-reduced-motion`.

## 11. Responsive Behavior

- At 1024px: side navigation reduces; comparison controls remain visible.
- At 768px: app shell becomes one column; bottom action bar may become sticky.
- Below 640px: tables become key-value cards, buttons use full width when paired decisions would become cramped.
- Maintain 17–18px body text and 48px primary targets on mobile.
- Do not hide critical totals, approval impacts, or status behind hover.

## 12. Accessibility

- Target WCAG 2.2 AA.
- Ensure keyboard order follows visual order.
- Provide visible focus states on every interactive control.
- Do not rely on color, icon, or position alone for meaning.
- Announce copied tokens, changed tabs, validation errors, and saved states.
- Use `aria-current`, `aria-selected`, and semantic tables where applicable.

## 13. Voice & Microcopy

Speak like an expert who translates complexity.

- Prefer: “처음 견적보다 38만 원이 추가됐어요.”
- Avoid: “변경 견적이 발생했습니다.”
- Prefer: “어디에서 가격 차이가 났는지 보여드릴게요.”
- Avoid: “공종별 상세 견적을 비교하세요.”
- Keep actions concrete: “시안 확정”, “업체 비교”, “변경 승인”, “보류”.

## 14. Do / Don't

Do:

- Let whitespace and alignment create calm.
- Use warm imagery next to precise data.
- Keep one primary decision per viewport.
- Preserve versions and explain every material difference.
- Use ZIP motifs as structural navigation.

Don't:

- Use blue-purple gradients, neon, or dark-first dashboards.
- Put every element inside a rounded card.
- Use green as a decorative page background.
- Hide scope differences behind a single total price.
- Use generic AI sparkle icons as the main brand device.
- Use aspirational interior copy without decision evidence.

## 15. Agent Prompt Guide

Bias toward White + Forest + Oak, structured comparison, warm imagery, thin borders, clear statuses, tabular prices, and calm Korean microcopy.

Reject generic dashboard chrome, excessive cards, glassmorphism, cold blue SaaS styling, decorative gradients, and lowest-price-first layouts.

Before completing a screen ask:

1. What decision is the user making here?
2. Are alternatives shown under the same conditions?
3. Is cost, schedule, or scope impact visible before approval?
4. Will this action leave a clear record?
5. Can a non-expert understand the copy without a contractor translating it?
