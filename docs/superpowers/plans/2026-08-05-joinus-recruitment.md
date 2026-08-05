# 真知招聘页优化 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** 将静态招聘页升级为表达 AI Native 文化、支持岗位切换和便捷投递的响应式单页。

**Architecture:** 保留现有 `index.html` 与 `css/style.css` 结构，重写页面内容与样式；岗位数据以内联 JavaScript 对象维护，按钮事件驱动右侧详情更新。图片与品牌链接继续使用现有本地资产和主站 URL。

**Tech Stack:** 原生 HTML5、CSS3、Vanilla JavaScript，无构建步骤、无外部运行时依赖。

---

### Task 1: Rewrite page structure and content

**Files:**
- Modify: `index.html`

- [ ] Replace stale two-job markup with Hero, identity, principles, role workspace, application CTA, and footer sections from the design spec.
- [ ] Add semantic role navigation buttons with `data-role` values and an empty detail panel populated by script.
- [ ] Add inline `roles` data and `renderRole()`/event listeners for all four positions.
- [ ] Add `mailto:` and `tel:` actions with exact supplied contact details and subject format.

### Task 2: Rebuild responsive visual system

**Files:**
- Modify: `css/style.css`

- [ ] Define typography, colors, section spacing, focus states, and reusable layout primitives.
- [ ] Preserve full-screen `hero-bg.jpg` hero with readable overlay, CTA, and visible next-section hint.
- [ ] Style principles as a five-item grid and roles as two-column navigation/detail workspace.
- [ ] Add mobile breakpoints for navigation, hero sizing, principle grid, role tabs, and application panel without horizontal overflow.

### Task 3: Verify behavior and responsive layout

**Files:**
- Test: `index.html`, `css/style.css`

- [ ] Run a local static server and load the page at desktop and mobile viewport widths.
- [ ] Verify each role button updates title, summary, responsibilities, requirements, bonuses, and tags.
- [ ] Verify all links resolve to the expected URLs and no console errors occur.
- [ ] Use `git diff --check` and inspect final status before reporting completion.
