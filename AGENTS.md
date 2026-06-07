# AGENTS.md — Sejamos 1 (Guerreiro em Cristo)

Projeto cristão de evangelização — arte + site Hugo em GitHub Pages. Imagem de guerreiro com armadura (Efésios 6) e 3 trilhas de conteúdo. Site: https://sejamos1.github.io

## Estrutura

```
content/
  _index.md                # Homepage com 3 cards de trilha
  trilha-1/                # 7 páginas Markdown
    pagina-1.md .. 7.md
  trilha-2/                # 6 páginas Markdown (apologética)
    _index.md
    pagina-1.md .. 6.md
  trilha-3/                # 6 páginas Markdown (discipulado)
    _index.md
    pagina-1.md .. 6.md
config/_default/
  hugo.toml                # Config principal (Tailwind build, módulos)
  params.toml              # Params (autor, aparência)
  languages.pt-br.toml     # Idioma português
  menus.pt-br.toml         # Menus
  markup.toml              # Markdown config (unsafe = true)
layouts/
  _default/
    baseof.html            # Template base (HTML shell)
    list.html              # Lista de páginas (trilha index)
    single.html            # Página única de leitura
  index.html               # Homepage custom (hero + 3 cards)
  partials/
    css.html               # Processamento Tailwind (css.TailwindCSS)
    header.html            # Header sticky com navegação
    footer.html            # Footer navy 3 colunas
    navigation.html        # Botão "Próximo →" zero decision
    sharing.html           # Barra de compartilhamento
    icon.html              # Ícones SVG inline
  shortcodes/
    icon.html              # Shortcode {{< icon >}} p/ markdown
assets/
  css/
    main.css               # Tailwind v4 + tema navy/gold
  images/
    patch-armadura-de-deus.png  # Imagem original (processada p/ WebP)
.github/workflows/deploy.yml    # CI: build + deploy no push para main
```

## Comandos

```bash
./hugo server -D            # Dev server com drafts
./hugo --minify             # Build de produção
```

Hugo extended v0.162.1 está no repositório (`./hugo`). Adicionado ao `.gitignore`.

## Arquitetura

- **Plataforma**: GitHub Pages + Hugo static site generator
- **CSS**: Tailwind v4 nativo via Hugo `css.TailwindCSS` (sem tema externo)
- **Domínio**: sejamos1.github.io (definitivo)
- **Conteúdo**: Markdown versionado no git, cada página é um `.md`
- **Deploy**: Automático via GitHub Actions (push na `main`)
- **QR Code**: Separado da imagem (não integrado no escudo)
- **Imagem**: PNG inicial; vetorização futura em Inkscape ou freelancer

## Conteúdo

- 3 trilhas baseadas em perfil do visitante
- Trilha 1 (curioso): **pronta** — 7 páginas em `content/trilha-1/`
- Trilha 2 (conhecedor): **pronta** — 6 páginas em `content/trilha-2/`
- Trilha 3 (cristão): **pronta** — 6 páginas em `content/trilha-3/`
- Versículos base: Efésios 6:10-18 (armadura) e João 17:21 (unidade)
- Site compilado: 37 páginas

## Próxima sessão — Contexto para retomar

### ⚠️ O que NÃO foi feito (pendente)
1. **⬅ PRIORIDADE: Revisão de conteúdo (Trilha 1)** — textos genéricos. Melhorar tom com cenários cotidianos, perguntas retóricas, linguagem direta. Ex: "Você sabe o nome do presidente. Sabe o cargo. Mas conhece ele? É assim que muita gente está com Jesus."
2. Revisão de conteúdo (Trilha 2) — mais apologética, estrutura problema→evidência→conclusão
3. Dark mode (`prefers-color-scheme`)
4. Open Graph / Twitter Cards para preview ao compartilhar
5. Página 404
6. Lighthouse audit

### Sessão 6 (07/06/2026) — o que foi feito
- **Problema resolvido**: deploy falhava porque `node_modules/` no `.gitignore` e CI não rodava `npm install`. Hugo `css.TailwindCSS` precisa do Tailwind CLI.
- **Fix**: adicionado `npm ci` no `.github/workflows/deploy.yml` antes do `hugo --minify`
- Site online com layout novo (Navy/Gold) mas conteúdo da Trilha 1 **ainda sem revisão**
- **IMPORTANTE**: Trilha 1 no site ainda reflete o texto original, não as melhorias planejadas

### Melhorias nos textos (trilha 1 e 2)
- Trilha 1: mais concreto, cenários cotidianos, perguntas retóricas, linguagem direta
- Trilha 2: mais apologética (dados/evidências), estrutura problema→evidência→conclusão
- Padrão: trocar afirmações abstratas por exemplos reais e contrastes

### Stack técnica (não mudar)
- Hugo + Tailwind v4 nativo (css.TailwindCSS) — sem PostCSS, sem webpack
- Zero frameworks JS (se precisar interatividade: HTMX ou Alpine.js)
- Markdown = única fonte de verdade
- package.json apenas para Tailwind (não virar projeto Node)
- Hugo binário versionado no repo (`./hugo`)

## Documentos .docx

`.docx` é zip. Extrair com `python3` via `zipfile` + `xml.etree.ElementTree`. Ver `files/PROGRESSO.md` para comando exato.
