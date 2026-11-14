# OpenPlay

**Central pessoal de entretenimento, descoberta e aprendizado.**

O OpenPlay reúne diretórios e links para encontrar filmes, séries, música, podcasts, documentários, jogos e conteúdos educativos gratuitos. O projeto começa com foco no Brasil e em português brasileiro (PT-BR).

## Estado atual

Primeira versão funcional da interface:
- Painel inicial e navegação por categorias.
- Catálogo inicial de plataformas e fontes.
- Pesquisa por título, tema e plataforma.
- Favoritos salvos localmente no navegador.
- Preferências de interesses.
- Recomendador inicial "O que eu consumo hoje?".
- Layout responsivo.
- Estrutura PWA e cache básico da interface.

## Importante sobre gratuidade e legalidade

O OpenPlay é um guia independente, não hospeda nem redistribui obras. Os links levam às plataformas oficiais. A disponibilidade pode variar por país, título, período e condições da plataforma. A indicação de acesso é orientativa: confirme na fonte oficial se o item é gratuito, se exige cadastro, se contém anúncios e quais são os termos de uso. Em acervos com licenças variadas, verifique a licença de cada obra.

## Executar localmente

Como é um projeto estático, basta abrir `index.html` no navegador. Para testar PWA e Service Worker, use um servidor local, por exemplo a extensão Live Server do VS Code ou:

```bash
python -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Publicar com GitHub Pages

**Ativação inicial obrigatória (uma única vez):**

1. Abra [Settings → Pages](https://github.com/mpjbiologo/openplay/settings/pages) no repositório.
2. Em **Build and deployment**, localize **Source** e selecione **GitHub Actions**.
3. Salve, se o GitHub solicitar.

Depois disso, o workflow `.github/workflows/pages.yml` publicará automaticamente a cada atualização da branch `main), ou poderá ser iniciado manualmente em **Actions → Deploy OpenPlay to GitHub Pages → Run workflow**.

- Acompanhe as execuções em [Actions](https://github.com/mpjbiologo/openplay/actions).
- O endereço esperado será https://mpjbiologo.github.io/openplay/.

**Importante:** o workflow não consegue criar o site Pages pela primeira vez usando apenas o `GITHUB_TOKEN`. Se o Pages ainda não estiver habilitado, a etapa `configure-pages` recebe `404 Not Found`. É necessário fazer a ativação inicial nas configurações do repositório, com permissão de administrador. Depois, os próximos deploys serão automáticos.

## Estrutura

```
.
├── index.html
├── manifest.webmanifest
├── sw.js
├── assets/
│   ├── css/style.css
│   ├── js/app.js
│   └── img/favicon.svg
└── README.md
```

## Próximas etapas

- Expandir e revisar o catálogo brasileiro por categoria.
- Criar uma ficha detalhada por plataforma e conteúdo.
- Registrar data e fonte de verificação de disponibilidade.
- Melhorar recomendações com preferências e filtros por duração.
- Criar grade semanal, playlists e maratonas.
- Avaliar integrações oficiais (APIs, RSS e players incorporados) respeitando limites e termos.
- Adicionar internacionalização.
- Criar testes automatizados e fluxo de atualização do catálogo.

## Privacidade

Nesta versão, favoritos e preferências ficam no armazenamento local do navegador. Não há conta, sincronização ou envio desses dados para um servidor.

## Licença

A definir pelo mantenedor. O conteúdo de terceiros permanece sujeito aos direitos e licenças de seus respectivos titulares.

## Changelog

### 2026-11-14 — 12h (BRT)
- Atualização do workflow: checkout v6, upload-pages-artifact v4 e runner Ubuntu 24.04.
- Documentação da ativação inicial obrigatória do GitHub Pages e da causa do erro 404.

### 2026-11-14
- Criação da estrutura inicial do OpenPlay.
- Implementação do painel, catálogo, pesquisa, favoritos e recomendador inicial.
- Adição de layout responsivo e estrutura PWA.
