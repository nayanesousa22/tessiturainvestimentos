# FXology: Design System (extraído do conceito da landing page)

> Fonte: vídeo/poster do shot "FXology Landing Page Concept" (Dribbble). Os valores são **estimados visualmente** a partir da imagem, não de CSS real. Ajuste com conta-gotas se precisar de precisão.

## 1. Conceito visual
Dark UI de fintech/prop firm. Fundo grafite quase preto, **um único acento verde neon**, bordas finas translúcidas, grade arquitetônica com nós nos cruzamentos, glows radiais suaves e títulos grandes com tracking apertado.

## 2. Cores

| Token | Hex | Uso |
|---|---|---|
| `--bg-canvas` | `#050C06` | Fundo externo (esverdeado) |
| `--bg-page` | `#0E0F11` | Fundo da página |
| `--bg-card` | `#141518` – `#181A1D` | Cards e containers |
| `--bg-elevated` | `#1C1E22` / `#22252A` | Pills, inputs, item ativo do menu |
| `--border-subtle` | `rgba(255,255,255,.06)` | Bordas de cards |
| `--border-strong` | `rgba(255,255,255,.18)` | Botão secundário |
| `--text-primary` | `#FFFFFF` / `#F3F4F6` | Títulos |
| `--text-secondary` | `#8E9299` / `#9CA3AF` | Corpo |
| `--text-tertiary` | `#60646C` | Legendas, rodapé legal |
| `--accent` | `#55E67E` / `#4ADE80` | Ícones, setas, linhas iluminadas, CTA |
| `--accent-light` | `#86EFAC` / `#B8F5CE` | Fim do gradiente dos títulos |
| `--accent-deep` | `#22C55E` | Glow |

**Gradiente do logo:** `linear-gradient(135deg, #7CF89B, #2EC964)`.
**Gradiente de título:** `linear-gradient(180deg, #FFFFFF, #B8F5CE)` com `background-clip: text`.

**Metais dos planos (cards "Choose your account"):**

| Plano | Símbolo | Cor (de → até) | Glow |
|---|---|---|---|
| Copper | Cu | `#9A5635` → `#C4754B` | laranja/cobre |
| Silver | Ag | `#7D8590` → `#CBD5E1` | cinza azulado |
| Gold | Au | `#A8893D` → `#DFC066` | dourado |
| Platinum | Pt | `#6B7280` → `#B4BCC8` | cinza |
| Rhodium | Rh | `#A1A1AA` → `#E4E4E7` | branco prateado |

## 3. Tipografia
- **Família:** sans geométrica/neo-grotesca moderna. Candidatas parecidas: **Plus Jakarta Sans** (mais provável), Satoshi, General Sans, Inter Tight. As letras "Cu/Ag/Au" e o "How it works" lembram Plus Jakarta Sans.
- Títulos com tracking bem fechado e peso leve (400–500).

| Papel | Tamanho (desktop 1440) | Peso | Tracking | Line-height |
|---|---|---|---|---|
| H1/H2 de seção | 44–56px | 400–500 | -0.03 a -0.04em | 1.1 |
| Título de card | 18–22px | 500 | -0.02em | 1.25 |
| Corpo | 13–14px | 400 | 0 | 1.5 |
| Pill / eyebrow | 11–12px | 500 | 0 | 1 |
| Título coluna rodapé | 11px | 600, MAIÚSCULAS | 0.06em | 1 |
| Símbolo químico (Cu, Ag...) | ~110–140px | 300–400 | -0.02em | 1 |
| Sigla de plataforma (MT4, MT5, DX) | ~100px | outline 1px | | |

Detalhe: nome do plano com colchete em **superscript** (`Cu`<sup>[Copper]</sup>).

## 4. Layout, espaçamento e forma
- Container ~1140–1200px, centralizado, dentro de frame arredondado (~20–24px de raio).
- Padding vertical de seção: 100–140px.
- Grids: 3 colunas (gap ~20px). Planos em 3 + 2 centralizados. Payouts em 4 colunas escalonadas (2ª e 4ª mais altas). Bento 2×2 (1 card alto + 2 empilhados, gap ~18px).
- **Raios:** pill 999px · botão 10–12px · card 12–16px · banner 18px · ícone-box 10px · logo 7px.
- **Grade arquitetônica:** linhas de 1px em `#1E2024`, nós de ~6px nos cruzamentos, filetes verdes neon que deslizam pelas bordas.
- Parafusos/nós circulares nos 4 cantos do banner CTA.

## 5. Componentes

**Botão primário:** fundo `#FFF`, texto `#111214` medium, altura 40–44px, raio 10–12px. À direita, um quadradinho de 28–30px (raio 8px) em `#55E67E` com seta `→` escura.
**Botão secundário ("Free trial"):** transparente/`#141518`, borda `1px rgba(255,255,255,.18)`, texto `#E5E7EB`.
**Botão terciário ("Learn more >>>"):** fundo `#16181C`, borda `rgba(255,255,255,.08)`, raio 8px, três chevrons `>>>` à direita.
**Submit (form):** cinza `#52555A` inativo → branco com texto escuro ativo.
**Pill/eyebrow:** fundo `#1A1C20`, borda sutil, ícone de 4 pontos verde + texto 11–12px (ex.: "Step One", "Payouts").
**Navbar:** 3 zonas. Logo + seletor de idioma | pill central com 6 links (ativo: fundo `#25272B` + ícone verde) | CTAs.
**Segmented control (abas de plano):** pill escuro, aba ativa branca com texto preto.
**Card de plano:** ícone de elemento químico (quadrado), nível por 1–5 estrelas de 4 pontas, símbolo gigante com glow metálico, nome, descrição, "Learn more".
**Card de feature:** ícone verde em caixa 44px + título + texto cinza.
**Stepper vertical:** card único com 3 blocos separados por linhas e setas `v`.
**Accordion FAQ:** itens com divisória 1px, ícone `+`/`−` verde à direita.
**Input com botão acoplado:** campo escuro + "Submit" dentro da mesma caixa.
**Ícones sociais:** círculos `#25272B` (Discord, Telegram, Facebook, Instagram, X, TikTok).

## 6. Efeitos
- **Glow radial verde** suave no canto inferior esquerdo do hero e atrás do título de Payouts.
- **Spotlight no hover** dos cards (cor do metal ou verde-oliva).
- **Linhas de borda iluminadas** em verde que percorrem divisórias.
- **Ondas finas** (1px) com pulsos de luz atrás dos cards do Step Two.
- **Constelação** (nós brancos com glow ligados por linha fina) no processo de avaliação.
- **Orbe verde + equações flutuantes + piso em grade 3D** no CTA final; piso em perspectiva também no rodapé.
- **Moeda 3D metálica** rotativa com texto "XRP" no hero.
- Títulos animam palavra por palavra.

## 7. Estrutura da página
1. Navbar
2. Hero ("How it works") com moeda 3D + 2 CTAs
3. Step One: escolha de conta (5 planos)
4. Step Two: personalização (3 add-ons)
5. Step Three: processo de avaliação (abas + stepper)
6. Escolha de plataforma (MT4, MT5, DXtrade)
7. Payouts (hero central + 4 colunas)
8. FAQ (2 colunas + accordion)
9. Banner CTA ("Stop losing your own money")
10. Bento: newsletter + Telegram + Discord
11. Rodapé (logo, redes, 3 colunas de links, piso em grade verde)

## 8. Tokens CSS prontos

```css
:root {
  --bg-canvas:#050C06; --bg-page:#0E0F11; --bg-card:#141518; --bg-elevated:#1C1E22;
  --border-subtle:rgba(255,255,255,.06); --border-strong:rgba(255,255,255,.18);
  --text-primary:#F3F4F6; --text-secondary:#8E9299; --text-tertiary:#60646C;
  --accent:#55E67E; --accent-light:#B8F5CE; --accent-deep:#22C55E;
  --metal-cu:#C4754B; --metal-ag:#CBD5E1; --metal-au:#DFC066; --metal-pt:#B4BCC8; --metal-rh:#E4E4E7;
  --radius-pill:999px; --radius-btn:10px; --radius-card:14px; --radius-banner:18px;
  --font:'Plus Jakarta Sans',system-ui,sans-serif;
}
body{background:var(--bg-page);color:var(--text-secondary);font:400 14px/1.5 var(--font)}
h1,h2{color:#fff;font-weight:500;letter-spacing:-.035em;line-height:1.1;
  background:linear-gradient(180deg,#fff,var(--accent-light));-webkit-background-clip:text;color:transparent}
.card{background:var(--bg-card);border:1px solid var(--border-subtle);border-radius:var(--radius-card)}
.btn-primary{display:inline-flex;align-items:center;gap:12px;height:42px;padding:0 6px 0 16px;
  background:#fff;color:#111214;border-radius:var(--radius-btn);font-weight:500}
.btn-primary .arrow{width:30px;height:30px;border-radius:8px;background:var(--accent);display:grid;place-items:center}
.btn-secondary{height:42px;padding:0 16px;border:1px solid var(--border-strong);border-radius:var(--radius-btn);color:#E5E7EB}
.pill{padding:6px 12px;border-radius:var(--radius-pill);background:#1A1C20;border:1px solid var(--border-subtle);font-size:12px}
```

## 9. Observações
- O mockup tem erros de grafia ("assesment", "Discrod", "training training"). Não copiar.
- O rodapé cita "FXIFY™ SOLUTIONS LIMITED". Troque por dados da sua marca.
- Os screenshots de referência estão em `C:\Users\Nayane\.gemini\antigravity\brain\13d648a7-98b9-431d-986e-12ae2e4db3fb\browser_sandbox\screenshots\`.
