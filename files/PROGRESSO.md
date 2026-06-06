# Progresso do Projeto — Somos 1

**Site**: https://sejamos1.github.io  
**Plataforma**: GitHub Pages + Hugo (static site generator)  
**Tema**: [hugo-paper](https://github.com/nanxiaobei/hugo-paper)

---

## Instruções para retomar sessão

Cole no início de cada nova conversa:

> Projeto cristão "Somos 1" (João 17:21). Imagem de guerreiro com Armadura de Deus (Efésios 6) + site Hugo em GitHub Pages. 3 trilhas de conteúdo. Repositório em `/mnt/c/dev/opencode/somos-1`. Hugo v0.162.1 (binário local `./hugo`). Deploy automático via GitHub Actions no push para `main`. Ver `files/PROGRESSO.md` e `AGENTS.md`.

---

## Estado atual

### ✅ Concluído

- Análise crítica do projeto (.docx → Markdown, QR separado, vetorização futura)
- Decisões de arquitetura: GitHub Pages + Hugo, domínio sejamos1.github.io
- Hugo extended v0.162.1 instalado (binário no repo, em `.gitignore`)
- Repositório git iniciado (branch `main`)
- Tema hugo-paper instalado como submodule
- `hugo.toml` configurado (pt-BR, menus, params)
- Site compila: 17 páginas, 749ms
- Homepage com 3 botões de trilha em `content/_index.md`
- Trilha 1 conteúdos migrados de .docx para Markdown (7 páginas, `content/trilha-1/`)
- Trilhas 2 e 3: placeholders como draft em `content/trilha-2/` e `trilha-3/`
- GitHub Actions workflow para deploy em `.github/workflows/deploy.yml`
- `AGENTS.md` atualizado com comandos e estrutura Hugo
- `files/PROGRESSO.md` criado para registro de sessões
- `.gitignore` configurado (hugo, swp, DS_Store)

### 🔄 Em andamento

- _(nada no momento)_

### 📋 Pendente

- [ ] **Vetorizar imagem do guerreiro** — Inkscape ou freelancer (fora do escopo atual)
- [ ] **Gerar QR Code** — `qrencode -s 10 -o qr.png 'https://sejamos1.github.io'`
- [ ] **Escrever Trilha 2** (conhecedor) — esboço em `files/`
- [ ] **Escrever Trilha 3** (cristão) — esboço em `files/`
- [ ] **Estamparia/cartões/redes sociais**

### Decisões tomadas

| Decisão | Escolha |
|---|---|
| Plataforma | GitHub Pages |
| Gerador estático | Hugo |
| Domínio | sejamos1.github.io |
| QR Code no escudo | ❌ Não — será separado da imagem |
| Arte final | Vetorização futura |
| Fonte do conteúdo | Markdown no git (única fonte de verdade) |

---

## Registro de sessões

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
1. Revisar conteúdo das 7 páginas (opcional)
2. Fazer push para GitHub e testar deploy
3. Iniciar escrita das Trilhas 2 e 3
4. Trabalhar na imagem/arte independentemente
