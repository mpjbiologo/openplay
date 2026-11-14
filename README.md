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

1. Abra **Settings → Pages** no repositório.
2. Em **Build and deployment**, selecione **GitHub Actions** como fonte.
3. O workflow `.github/workflows/pages.yml` publicará automaticamente a cada atualização da branch `main`.
4. Acompanhe a execução em **Actions → Deploy OpenPlay to GitHub Pages**.
5. O endereço esperado será https://mpjbiologo.github.io/openplay/.

Não há etapa de build nem dependências de instalação. A primeira publicação depende de habilitar GitHub Actions em Settings → Pages.

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

### 2026-11-14
- Criação da estrutura inicial do OpenPlay.
- Implementação do painel, catálogo, pesquisa, favoritos e recomendador inicial.
- Adição de layout responsivo e estrutura PWA.