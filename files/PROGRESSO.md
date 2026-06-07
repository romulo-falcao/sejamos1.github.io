# Progresso do Projeto — Sejamos 1

**Site**: https://romulo-falcao.github.io/sejamos1.github.io/  
**Repositório**: https://github.com/romulo-falcao/sejamos1.github.io  
**Plataforma**: GitHub Pages + Hugo (static site generator)  
**Tema**: Nenhum (Hugo + Tailwind v4 puro — Blowfish removido na Sessão 5)

---

## Instruções para retomar sessão

Cole no início de cada nova conversa:

> Projeto cristão "Sejamos 1" (João 17:21). Imagem de guerreiro com Armadura de Deus (Efésios 6) + site Hugo em GitHub Pages. 3 trilhas de conteúdo. Repositório em `/mnt/c/dev/opencode/somos-1`. Hugo v0.162.1 (binário local `./hugo`). **Sem tema** — Hugo + Tailwind v4 puro (css.TailwindCSS nativo). Deploy automático via GitHub Actions no push para `main`. Ver `files/PROGRESSO.md` e `AGENTS.md`.

---

## Estado atual

### ✅ Concluído

- Análise crítica do projeto (.docx → Markdown, QR separado, vetorização futura)
- Decisões de arquitetura: GitHub Pages + Hugo
- Hugo extended v0.162.1 instalado (binário no repo, em `.gitignore`)
- Repositório git iniciado (branch `main`)
- Tema atual: **Blowfish** (substituiu o Paper)
- Homepage personalizada com custom layout (hero + 3 cards)
- `config/_default/` com params, menus, i18n configurados
- Site compila: 21 páginas, ~2s
- Trilha 1 conteúdos migrados de .docx para Markdown (7 páginas, `content/trilha-1/`)
- Trilhas 2 e 3: placeholders (não-draft, link desabilitado visualmente)
- GitHub Actions workflow para deploy em `.github/workflows/deploy.yml`
- `AGENTS.md` atualizado com comandos e estrutura Hugo
- `files/PROGRESSO.md` criado para registro de sessões
- `.gitignore` configurado (hugo, swp, DS_Store, public/)
- **Push para GitHub e deploy automático funcionando** ✅

### 🔄 Em andamento

- _(nada no momento)_

### 📋 Pendente

- [ ] **Vetorizar imagem do guerreiro** — Inkscape ou freelancer (fora do escopo atual)
- [ ] **Gerar QR Code** — `qrencode -s 10 -o qr.png 'https://sejamos1.github.io'`
- [ ] **Vetorizar imagem do guerreiro** — Inkscape ou freelancer (fora do escopo atual)
- [ ] **Gerar QR Code** — `qrencode -s 10 -o qr.png 'https://sejamos1.github.io'`
- [ ] **Revisão de conteúdo (Trilha 1)** — textos ainda genéricos, precisam ficar mais concretos com cenários cotidianos
- [ ] **Revisão de conteúdo (Trilha 2)** — mais apologética baseada em dados
- [ ] **Ajustes de design (cores, hero, imagem quando pronta)**
- [ ] **Estamparia/cartões/redes sociais**
- [x] **Sessão 4: análise zero decision; imagens/ não trackeada**
- [x] **Sessão 5: migração Blowfish → Hugo + Tailwind v4 puro**

### Decisões tomadas

| Decisão | Escolha |
|---|---|
| Plataforma | GitHub Pages |
| Gerador estático | Hugo |
| CSS | Tailwind v4 nativo (css.TailwindCSS) |
| Tema anterior | ~~Blowfish~~ removido (Sessão 5) |
| URL | https://sejamos1.github.io |
| QR Code no escudo | ❌ Não — será separado da imagem |
| Arte final | Vetorização futura |
| Fonte do conteúdo | Markdown no git (única fonte de verdade) |

---

## Registro de sessões

### Sessão 6 — 07/06/2026

**O que foi feito**
- Diagnóstico: deploy não refletia mudanças porque `node_modules/` no `.gitignore` e CI sem `npm install`
- Workflow corrigido: adicionado `npm ci` antes do `hugo --minify` no `.github/workflows/deploy.yml`
- Deploy verificado: workflow `conclusion=success` e site online com as mudanças da Sessão 5

**Observação importante**
- As melhorias de conteúdo da **Trilha 1** (textos mais concretos, cenários cotidianos) **ainda não foram implementadas** — só o layout/migração técnica foi deployada
- Revisão de conteúdo continua pendente para a Trilha 1 (e Trilha 2)

**Estado atual**
- Site: Tailwind v4 + Navy/Gold funcionando online
- Deploy CI: corrigido e estável
- Conteúdo: ainda o mesmo texto original (genérico) das Trilhas 1, 2, 3

**Próximos passos sugeridos**
1. **⬅ PRIORIDADE: Revisão de conteúdo (Trilha 1)** — textos genéricos, melhorar tom com cenários cotidianos, perguntas retóricas, linguagem direta
2. **Revisão de conteúdo (Trilha 2)** — mais apologética, estrutura problema→evidência→conclusão
3. Adicionar dark mode via `prefers-color-scheme`
4. Open Graph / Twitter Cards para preview ao compartilhar
5. Página 404 customizada
6. Lighthouse audit (target 95+)
7. Remover links manuais de navegação duplicados do conteúdo Markdown
8. Gerar QR Code para estamparia

---

### Sessão 5 — 07/06/2026

**O que foi feito**
- Migração completa: Blowfish → Hugo + Tailwind v4 puro
- Setup: npm, Tailwind v4, `@tailwindcss/typography`, Hugo `css.TailwindCSS` nativo
- Paleta customizada **Navy + Gold** (cores do guerreiro) via `@theme` no CSS
- Base template `baseof.html` com CSS processing via Hugo Pipes
- Header sticky com navegação + mobile menu
- Footer 3 colunas com trilhas e links
- Homepage redesenhada: hero full-width com armadura (WebP) + 3 cards + versículo
- Layout de lista (trilha index): cards numerados com círculos navy
- Layout de página única: limpa, sem sidebar/breadcrumbs, com "Voltar" e título
- Navegação zero decision: botão "Próximo →" grande no fim de cada página (por peso)
- Compartilhamento: WhatsApp, Facebook, Telegram com ícones SVG
- Partial de ícones reutilizável (SVG inline) + shortcode `{{< icon >}}` compatibility
- Animação fade-in entre páginas
- Blowfish removido (submodule + diretório)
- Limpeza: `custom.css`, `versiculo-do-dia.html`, `versiculos.json`, `images/` duplicado
- `.gitignore` atualizado: `node_modules/`, `hugo_stats.json`
- `assets/css/custom.css` → deletado (substituído por `main.css`)
- Site compila: **39 páginas, 0 warnings, 0 erros, ~6s**

**Mudanças de design**
- Paleta: Ocean (azul/ciano) → Navy + Gold (sóbrio, solene)
- Hero: overlay azul → overlay navy com gradiente mais suave
- Cards: fundo branco → fundo cream (off-white)
- CTAs: azul primário → dourado quente
- Tipografia: mesma (system stack), versículos em itálico
- Footer: navy escuro com texto dourado nos links

**Estado atual**
- Site Hugo puro (sem tema), 39 páginas, Tailwind v4
- Homepage com herói + 3 cards + versículo
- Trilhas 1, 2, 3 completas (19 páginas de conteúdo)
- Navegação linear com botão "Próximo →"
- Compartilhamento social integrado
- Header/footer responsivos
- Pronto para deploy

**Práticas definidas para evitar churn tecnológico:**
- ❌ Não adicionar JavaScript frameworks (React, Vue, etc.)
- ✅ Markdown = única fonte de verdade (conteúdo ≠ apresentação)
- ✅ `package.json` usado APENAS para Tailwind (não virar projeto Node)
- ✅ Se precisar de interatividade futura: HTMX ou Alpine.js (leves)
- ✅ Hugo binário versionado no repositório (independe de versão do sistema)
- ✅ Tailwind v4 via Hugo nativo (sem PostCSS, webpack ou build externa)
- ✅ Conteúdo portável entre geradores estáticos (Markdown puro)

---

### Sessão 4 — 07/06/2026

**O que foi feito**
- Análise de "zero decision" aplicada ao projeto (ver notas abaixo)
- Verificação de deploy indevido: `images/patch-final-armadura-de-deus.png` não trackeado (ok)
- `.gitignore` confirmado: public/, resources/, files/, AGENTS.md, hugo — cobertura correta
- `sobre/`, `contato/`, `oracao/` páginas existentes e compilando
- Site compila com 37 páginas, sem erros
- PROGRESSO.md atualizado

**Análise Zero Decision — contexto para o projeto**

O conceito "zero decision" (fricção zero de decisão) aplicado ao desenvolvimento:
1. **Fluxo de conteúdo**: Markdown no git é fonte única — zero decisão sobre formato/editor
2. **Deploy**: push na main → GitHub Actions → publicado — zero decisão de infra
3. **Preview local**: `./hugo server -D` — zero decisão de setup
4. **Tema Blowfish**: custom layout na homepage, Tailwind embutido — zero decisão de framework CSS

Aplicado à UX do site:
- Homepage já segmenta por perfil (cards) — bom
- Cada trilha é linear (weight 1..N) — bom
- **Oportunidade**: botão "Próximo →" proeminente no final de cada página (em vez de links de texto misturados ao conteúdo). Usuário não precisa decidir "o que fazer agora" — o caminho é óbvio.
- **Oportunidade**: navegação entre trilhas já implementada (fim da T1 → T2, fim da T2 → T3) — manter.
- **Oportunidade**: remover links de navegação lateral/header desnecessários durante a leitura de uma trilha (foco na progressão linear).

**Observação**: verificar antes de cada push se `images/`, `static/`, `assets/` contêm arquivos que não deveriam ser publicados. Atualmente `images/patch-final-armadura-de-deus.png` está untracked (correto). O WebP processado fica em `assets/` e é servido pelo Hugo.

---

### Sessão 3 — 06/06/2026

**O que foi feito**
- Extraído conteúdo do `files/Trilhas2e3_TextosSite.docx`
- Criadas 6 páginas Markdown para Trilha 2 (`content/trilha-2/pagina-1..6`)
- Criadas 6 páginas Markdown para Trilha 3 (`content/trilha-3/pagina-1..6`)
- Homepage atualizada: Trilhas 2 e 3 como links ativos (removido placeholder "Em breve")
- Menus e navegação atualizados (todas as trilhas no topo e footer)
- Trilha 1 página 7 atualizada com links diretos para Trilhas 2 e 3
- Site compila com 37 páginas, sem erros

**Estado atual**
- Site ao vivo em https://sejamos1.github.io com tema Blowfish
- Homepage com 3 cards clicáveis
- Trilha 1: 7 páginas
- Trilha 2: 6 páginas (apologética/base bíblica)
- Trilha 3: 6 páginas (discipulado/Efésios 6/João 17)

**Próximos passos**
1. Revisão ortográfica e refinamento de conteúdo (todas as trilhas)
2. Ajustes de design quando imagem do guerreiro estiver pronta
3. Gerar QR Code para estamparia

---

### Sessão 1 — 06/06/2026

**O que foi feito**
- Análise crítica: fraquezas dos .docx, PNG raster, WordPress gratuito, fluxo manual
- Decisões: GitHub Pages + Hugo, domínio sejamos1.github.io, QR separado
- Hugo extended v0.162.1 instalado no repo
- Git init, branch main, .gitignore
- Tema hugo-paper como submodule
- Config hugo.toml (pt-BR, menus, params)
- Site compila (17 páginas)
- Homepage com 3 botões de trilha
- Trilha 1 convertida: .docx → 7 páginas Markdown
- Placeholders para Trilhas 2 e 3 (draft)
- CI: GitHub Actions workflow para deploy
- AGENTS.md e PROGRESSO.md atualizados

**Estado atual**
- Site Hugo funcional, conteúdo da Trilha 1 em Markdown
- Imagem do guerreiro não integrada ao site (será trabalhada separadamente)
- Repositório local pronto para primeiro push

**Próximos passos**
1. Revisar design da homepage e ajustar cores/esquema (Blowfish "ocean")
2. Adicionar imagem do guerreiro no hero quando estiver pronta
3. Refinar página da Trilha 1 com estilo Blowfish
4. Iniciar escrita das Trilhas 2 e 3
5. Trabalhar na imagem/arte independentemente
