# Progresso do Projeto — Sejamos 1

**Site**: https://romulo-falcao.github.io/sejamos1.github.io/  
**Repositório**: https://github.com/romulo-falcao/sejamos1.github.io  
**Plataforma**: GitHub Pages + Hugo (static site generator)  
**Tema**: [hugo-paper](https://github.com/nanxiaobei/hugo-paper)

---

## Instruções para retomar sessão

Cole no início de cada nova conversa:

> Projeto cristão "Sejamos 1" (João 17:21). Imagem de guerreiro com Armadura de Deus (Efésios 6) + site Hugo em GitHub Pages. 3 trilhas de conteúdo. Repositório em `/mnt/c/dev/opencode/somos-1`. Hugo v0.162.1 (binário local `./hugo`). Deploy automático via GitHub Actions no push para `main`. Ver `files/PROGRESSO.md` e `AGENTS.md`.

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
- [ ] **Revisão ortográfica e refinamento de conteúdo (Trilhas 1, 2, 3)**
- [ ] **Ajustes de design (cores, hero, imagem quando pronta)**
- [ ] **Estamparia/cartões/redes sociais****

### Decisões tomadas

| Decisão | Escolha |
|---|---|
| Plataforma | GitHub Pages |
| Gerador estático | Hugo |
| Tema | Blowfish (custom layout) |
| URL | https://sejamos1.github.io |
| QR Code no escudo | ❌ Não — será separado da imagem |
| Arte final | Vetorização futura |
| Fonte do conteúdo | Markdown no git (única fonte de verdade) |

---

## Registro de sessões

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
