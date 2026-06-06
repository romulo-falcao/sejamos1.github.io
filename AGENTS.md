# AGENTS.md — Sejamos 1 (Guerreiro em Cristo)

Projeto cristão de evangelização — arte + site Hugo em GitHub Pages. Imagem de guerreiro com armadura (Efésios 6) e 3 trilhas de conteúdo. Site: https://romulo-falcao.github.io/sejamos1.github.io/

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
  hugo.toml                # Config principal
  params.toml              # Blowfish theme params
  languages.pt-br.toml     # Idioma português
  menus.pt-br.toml         # Menus
  markup.toml              # Markdown config
layouts/partials/home/
  custom.html              # Homepage custom (hero + 3 cards)
themes/blowfish/           # Tema (submodule)
files/
  PROGRESSO.md             # Registro de sessões + estado atual
  Projeto_GuerreiroEmCristo.docx
  Trilha1_Textos*.docx     # Fonte original (manter como referência)
  Trilhas2e3_TextosSite.docx
images/
  patch-armadura-de-deus.png
.github/workflows/deploy.yml  # CI: build + deploy no push para main
```

## Comandos

```bash
./hugo server -D            # Dev server com drafts
./hugo --minify             # Build de produção
```

Hugo extended v0.162.1 está no repositório (`./hugo`). Adicionado ao `.gitignore`.

## Arquitetura

- **Plataforma**: GitHub Pages + Hugo static site generator
- **Tema**: Blowfish (Tailwind CSS, custom layout na homepage)
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

## Documentos .docx

`.docx` é zip. Extrair com `python3` via `zipfile` + `xml.etree.ElementTree`. Ver `files/PROGRESSO.md` para comando exato.
