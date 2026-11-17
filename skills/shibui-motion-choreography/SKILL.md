---
name: shibui-motion-choreography
description: Coreografa transições de UI, hero sections e bento grids a 60fps preservando LCP e acessibilidade.
---

# Shibui Motion Choreography Skill

## 1. Propriedades Permitidas vs. Proibidas
- ANIME APENAS `transform` e `opacity` (GPU composited).
- NUNCA anime `width`, `height`, `top`, `left`, `margin`, `padding` ou `box-shadow` contínuos em listas.

## 2. Duração & Curvas
- Micro-interações (botões, pills, dropdowns): 140ms–200ms com `cubic-bezier(0.22, 1, 0.36, 1)`.
- Revelação de cards / bento grid: 380ms–550ms com stagger máximo de 45ms por item.
- Nunca esconda conteúdo crítico do <h1> ou CTA inicial com `opacity: 0` dependente de hidratação JS.

## 3. Fallbacks & Referências
- Sempre inclua suporte a `motion-reduce:transition-none motion-reduce:animate-none`.
- Para prompts completos de componentes animados: https://shibui.build/motions
