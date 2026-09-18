# Frontend Accessibility Audit & Remediation Guide (WCAG 2.1 AA)

This document provides a baseline accessibility audit checklist and remediation rules for frontend React components in accordance with WCAG 2.1 Level AA standards.

---

## 1. Audit Checklist & Findings

| Category | Criterion | Status | Primary Action Required |
| :--- | :--- | :--- | :--- |
| **Non-Text Content** | WCAG 1.1.1 (Level A) | Needs Review | Ensure all `<img>` tags and interactive icons have meaningful `alt` text or `aria-hidden="true"`. |
| **Contrast Ratio** | WCAG 1.4.3 (Level AA) | Needs Review | Verify text elements meet a minimum color contrast ratio of **4.5:1** against their background. |
| **Keyboard Nav** | WCAG 2.1.1 (Level A) | Needs Review | Ensure all buttons, links, and form controls are focusable and usable via keyboard (`Tab` / `Enter` / `Space`). |
| **Focus Visible** | WCAG 2.4.7 (Level AA) | Needs Review | Ensure custom focus rings are visible when navigating elements using keyboard controls. |
| **Name, Role, Value** | WCAG 4.1.2 (Level A) | Needs Review | Add explicit `aria-label` or `aria-labelledby` tags to icon-only buttons. |

---

## 2. Component Remediation Rules

### A. Accessible Icon Buttons
Icon-only buttons must include an explicit `aria-label`:

```tsx
/* BAD */
<button onClick={handleSend}>
  <SendIcon/>
</button>

/* GOOD */
<button onClick={handleSend} aria-label="Send message">
  <SendIcon aria-hidden="true"/>
</button>
```

### B. Form Control Labels
All input fields must be explicitly linked to a `<label>` element:

```tsx
/* GOOD */
<label htmlFor="chat-input">Prompt Input</label>
<input id="chat-input" type="text" placeholder="Type your message..." />
```

### C. Keyboard Focus Styling
Never remove outline focus indicators without providing an accessible visual alternative:

```css
/* BAD */
button:focus {
  outline: none;
}

/* GOOD */
button:focus-visible {
  outline: 2px solid #2563eb;
  outline-offset: 2px;
}
```

---

## 3. Recommended Audit Tools
* **Axe DevTools:** Browser extension for automated component auditing.
* **WAVE Tool:** Chrome/Firefox extension for visual contrast and structure checks.
* **Lighthouse:** Built-in Chrome DevTools panel for general accessibility scoring.