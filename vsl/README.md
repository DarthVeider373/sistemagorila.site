# Clone — Máquina Hydra VSL (pv/ld3/297)

Clone estático fiel da página original `https://maquinahydra.com.br/pv/ld3/297/`.

## Estrutura

```
clone-maquinahydra-vsl/
├── index.html              ← página principal (idêntica à original)
├── styles/main.css         ← CSS (Tailwind compilado, baixado do site original)
├── scripts/main.js         ← lógica do pitch condicional + anti-voltar
├── assets/images/          ← 14 imagens baixadas (capa, prints de depoimento, bônus etc.)
└── README.md
```

## Como usar

Abra `index.html` direto no navegador, ou sirva com qualquer servidor estático:

```bash
npx serve .
```

## Pontos importantes (não removidos, mas você deve revisar antes de publicar)

1. **Player de vídeo (VSL)**: o vídeo é carregado via script de terceiro
   (`vturb-smartplayer`, hospedado em `scripts.converteai.net` com o ID
   `93013c20-512e-4b2b-84d6-a05a7b1fc8cf/ab-test/6a2041a94d1de417672b4967`).
   Esse player **não pertence a você** — ele está atrelado à conta ConverteAI/Vturb
   do dono do site original. Para usar seu próprio vídeo, você precisa criar
   uma conta em um serviço de VSL player (ex: Vturb/ConvertAI, Panda Video,
   Vimeo) e trocar o ID em `index.html` e `scripts/main.js`.

2. **Links de checkout**: apontam para
   `https://checkout.payt.com.br/99c88b67cba952c90137c513aa87c025?split=12`
   (checkout Payt do dono original) e para `https://pay.hub.la/oLp2SD7lTjhdiINou2PX`
   (Hubla, usado no pitch B). **Troque pelos seus próprios links de checkout**
   antes de usar comercialmente — senão qualquer venda vai para a conta original.

3. **Pixels/Tags**: `GTM-5XG6PL48` (Google Tag Manager) e o script da Utmify
   são do dono original. Troque pelos seus próprios IDs de rastreamento.

4. **Script anti-voltar (`noback`)**: em `scripts/main.js`, intercepta o botão
   "voltar" do navegador e redireciona para `/back1/297` ou `/back2/247`
   (páginas de downsell que não existem neste clone — ajuste ou remova as rotas).

5. **`vturb-smartplayer` dispara eventos** (`player:ready`) que controlam
   quando o resto da página (`.esconder`) aparece — isso só funciona quando
   o player de vídeo real estiver configurado corretamente.

## O que foi baixado

- HTML completo (estrutura, textos, classes Tailwind) — idêntico ao original
- CSS compilado (`style-DeMmMMuo.css`, 73KB)
- 14 imagens: `fav.png`, `capa.webp`, `print1-6.webp`, `sala-vip.webp`,
  `socio-hydra.webp`, `bau.webp`, `mentorias-semanais.webp`, `todos-new.webp`,
  `garantia.webp`
