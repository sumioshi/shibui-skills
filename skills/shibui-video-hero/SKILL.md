---
name: shibui-video-hero
description: Implementa backgrounds em vídeo MP4 em loop para hero de sites mantendo legibilidade, iOS autoplay e Core Web Vitals saudáveis.
---

# Shibui Video Background Skill

Ao adicionar vídeo em loop como fundo de hero ou seção:

## 1. Tag HTML5 Obrigatória
Use sempre:
```html
<section class="relative isolate overflow-hidden bg-neutral-950">
  <video
    class="pointer-events-none absolute inset-0 -z-20 h-full w-full object-cover"
    autoplay
    loop
    muted
    playsinline
    poster="/poster.webp"
    src="https://media.shibui.build/..."
  ></video>
  <div aria-hidden="true" class="absolute inset-0 -z-10 bg-gradient-to-b from-black/55 via-black/35 to-black/75"></div>
  <!-- Conteúdo do hero aqui -->
</section>
```

## 2. Proteções de Performance & Acessibilidade
- Nunca omita `muted` nem `playsinline`: o Safari iOS bloqueia autoplay sem ambos.
- Defina sempre cor de fundo escura no container pai (`bg-neutral-950`) e `poster` leve para primeira pintura imediata.
- Respeite `@media (prefers-reduced-motion: reduce)` pausando ou ocultando movimento contínuo para quem prefere tela estática.
- Catálogo pronto: https://shibui.build/backgrounds
