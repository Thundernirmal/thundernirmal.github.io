AGENTS.md

Repo: Dark-mode-only static site using HTML + Tailwind CDN.

Build/lint/test
- Build: None; open index.html or python3 -m http.server 8000
- Tailwind: CDN <script src="https://cdn.tailwindcss.com"></script> with inline tailwind.config in index.html
- Lint HTML: npx htmlhint . (optional)
- Lint CSS: Tailwind utilities inline; if custom CSS added, npx stylelint "**/*.css"
- Tests: None. If adding E2E, use Playwright; single: npx playwright test path/to/spec -g "name"

Code style
- Formatting: 2-space indent, LF, UTF-8; semantic HTML; double-quoted attrs
- Tailwind: utility-first; prefer inline classes; group logically; define colors/fonts in tailwind.config extend
- Theme: dark-mode only; use slate-100 text on deep navy gradient backgrounds; glass surfaces bg-white/5 with borders white/10
- Components: cards use rounded-2xl, border, bg-white/[.04], backdrop-blur, shadow; buttons must NOT use gradients (solid fills only); use subtle ghost styles
- JS: minimal; smooth scroll and IntersectionObserver; avoid globals if adding more
- Naming: files kebab-case; ids lower-kebab; components PascalCase if added
- Accessibility: high contrast, focus-visible, skip link, reduced-motion support
- Performance: optimize images, prefer CSS transforms/opacity for animations

Cursor/Copilot
- No project-specific rules; follow Tailwind-first dark-only approach.
