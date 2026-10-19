---
name: good-software
description: Principles of good, enterprise-ready software. Use whenever designing, building, reviewing, or writing any user-facing software, feature, interface, or product copy — to check the work against design-system, accessibility, and security best practices.
---

# Good Software

Good, enterprise-ready software is **consistent, usable by everyone, and secure**. When building or reviewing anything user-facing, apply the three pillars below. Catch issues early; when unsure, follow the "Do" and avoid the "Don't".

## 1. Design Systems — consistency at scale

**Do**
- Reuse existing components and design tokens (shared values for color, spacing, and type) instead of inventing new ones.
- Keep naming and terminology consistent — one word per action, everywhere.
- Follow the documented voice (constant personality) and adjust tone to the situation.
- Document any genuinely new pattern so the system stays a single source of truth.

**Avoid**
- Hard-coding values (e.g. a raw color) when a token for it already exists.
- Rebuilding a component that already exists.
- Using different labels for the same action in different places.

## 2. Accessibility — usable by everyone

**Do**
- Aim for WCAG 2.2 AA; check work against POUR (Perceivable, Operable, Understandable, Robust).
- Give meaningful images alt text; write link text that names its destination.
- Keep text contrast at least 4.5:1; ensure full keyboard access and a logical heading structure.
- Write error messages that state the problem and how to fix it.

**Avoid**
- Signaling meaning with color alone.
- Vague links ("click here"), missing alt text, keyboard traps, or auto-playing media.

## 3. Security — protect users and their data

**Do**
- Apply least privilege (minimum access needed) and defense in depth (multiple layers) by default.
- Validate and sanitize all input from users or outside sources; never trust it.
- Encrypt sensitive data; use proven, standard libraries rather than custom cryptography.
- Keep secrets (passwords, keys) out of the code; keep dependencies patched.
- For AI features: guard against prompt injection and limit how much the agent can act on its own.

**Avoid**
- Putting secrets in code or committing them to a repository.
- Trusting user input, writing your own encryption, or exposing internal details in error messages.

## Sources (authoritative)
- Design systems: Material Design (m3.material.io), IBM Carbon, Shopify Polaris
- Accessibility: W3C Web Accessibility Initiative / WCAG (w3.org/WAI)
- Security: OWASP (owasp.org), including the OWASP Top 10 for LLM Applications
