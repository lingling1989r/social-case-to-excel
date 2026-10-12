# social-case-to-excel

Transformar publicações sociais em casos rastreáveis, análises de métodos e documentos de pesquisa ilustrados.

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [हिन्दी](README.hi.md)

## Usos e entregas

Este fluxo reconstrói os primeiros passos internacionais das marcas, organiza casos de marketing social e analisa necessidades nos comentários. Hardware é apenas um exemplo; outros temas incluem publicidade com IA, lançamentos, comércio internacional e conteúdo.

- Excel: participantes, ações, resultados relatados, datas, fontes, categorias e limites das evidências.
- Métodos: etapas, requisitos e adaptações para diferentes marcas.
- Imagens dos posts, capas de vídeo ou capturas com legendas e fontes.
- Documento Markdown com descobertas e métodos; HTML quando solicitado.
- Lista de candidatos e exclusões para revisar o alcance da pesquisa.

## Dos exemplos às decisões

| Uso | Pesquisa | Objetivo |
| --- | --- | --- |
| Aquisição B2B | Canais, conteúdo, participação comunitária e resultados relatados | Planejar testes de canais e conteúdo |
| Marcas e lançamento internacional | Atividades iniciais de contas oficiais, usuários, mídia e moderadores | Criar cronologias e aprender métodos de lançamento |
| Publicidade criativa com IA | Conceitos de imagem/vídeo, técnicas e evidências de produção | Referências e prompts adaptáveis; prompts inferidos não são os originais |
| Pesquisa de mercado e produto | Usuários, tarefas, obstáculos e funções desejadas | Definir cenários e perguntas de validação |
| Análise competitiva | Posicionamento, funções, conjuntos e serviços | Hipóteses de diferenciação baseadas em evidências |
| Avaliações e reclamações | Elogios, queixas e barreiras reais de uso | Melhorar produto, FAQ e conteúdo; amostra pequena não mede participação de mercado |
| Comunidades Reddit | Discussões, regras, necessidades e posts promocionais | Participação útil sem depoimentos falsos nem publicações em massa |
| Escuta social do setor público | Políticas, feedback sobre serviços e discussões abertas | Sínteses neutras; atividade online não é pesquisa de opinião |
| Fornecedores no 1688 | Fornecedores, kits, SKUs, pedidos mínimos e preços por volume | Preparar candidatos e verificações; anúncios não certificam qualidade nem autorização |
| Preços entre marketplaces | 1688, Amazon, Temu e Walmart por modelo, quantidade e funções | Estudar ofertas de produto; diferença de preço não é lucro |

Comércio, fornecimento e temas públicos são fluxos adaptáveis, não funções integradas de um clique. Verifique ferramentas ClaudeBaby, campos e cobertura realmente disponíveis no ambiente e adapte o formato de saída.

## Pesquisas que realizamos

| Estudo | Intenção | Objetivo |
| --- | --- | --- |
| Primeiro ano internacional de marcas chinesas, X e Reddit | Encontrar ações iniciais e discussões não oficiais | Métodos de lançamento e comunidade |
| Aquisição social B2B | Entender confiança e consultas comerciais | Experimentos de canais |
| Sites independentes, SEO/GEO e Reddit | Excluir promoção pura e buscar processos documentados | Escolher métodos de busca, conteúdo e comunidade |
| Publicidade criativa com IA | Aprender conceitos para outras marcas | Referências e planos de produção, sem afirmar resultados de campanhas |
| ESP32 com agentes/IA | Buscar cenários úteis e reproduzíveis | Integração AuraBaba, demos e aquisição |
| Fornecimento ESP32 e ofertas internacionais | Verificar peças econômicas, kits completos e SKUs reais | Opções de compra e produto, sem afirmar compras, fabricação ou lucro |

Exemplos → métodos → usuários e necessidades → experimentos → fornecimento e conteúdo. Desenvolvimento, publicação, compra e conversão exigem execução e validação separadas.

## Exemplos de pedidos

- Pesquisar aquisição B2B do nosso setor com métodos, evidências e Excel ilustrado.
- Analisar avaliações e reclamações reais de concorrentes, separando originais e recomendações.
- Consultar kits completos no 1688 via ClaudeBaby: SKU, mínimos, peças e preços.
- Comparar fornecimento nacional e ofertas internacionais pelo mesmo modelo e quantidade.
- Resumir políticas e feedback de uma instituição pública de forma neutra em um período definido.

## Exemplo: o primeiro ano no exterior

Uma pesquisa histórica reuniu 44 eventos de OnePlus, Anker, Bambu Lab, Keychron, Snapmaker e EcoFlow. Separou pré-lançamento, primeiro ano e outros indícios iniciais, incluindo contas oficiais, mídia, moderadores e usuários. OnePlus: contatos com moderadores e perguntas a executivos; Keychron: compra por crowdfunding antes de compartilhar no Reddit; Bambu Lab: discussões sobre demos, materiais e entrega. Isso não comprova vendas atribuídas ao canal.

Trechos de uma planilha real: as capturas permanecem em chinês. Cobertura histórica não garante permissões atuais. Arquivos reais são apresentados por tema em [`outputs/`](outputs/).

### Análise de métodos

![Análise de métodos](assets/readme/methods.png)

### Adaptações para marcas

![Adaptações para marcas](assets/readme/brand-reference.png)

### Cronologia e evidências

![Cronologia e evidências](assets/readme/timeline.png)

## Utilização

Instale a pasta no diretório de skills suportado pelo Agent. Use `$social-case-to-excel` com tema, plataformas, período e número de casos. Exemplo: reconstruir o início internacional de marcas chinesas no X e Reddit com fontes oficiais e usuários, métodos, evidências e adaptações, em Excel e documento ilustrados. Python requer `openpyxl` e `Pillow`; scripts são modelos adaptáveis.

## Conexão de dados

**ClaudeBaby** é o único serviço de dados desta versão. Reddit, X, YouTube e Bilibili são plataformas pesquisadas; ferramentas e permissões determinam a cobertura. No primeiro uso, verifique conexão MCP existente e capacidades necessárias; cadastre e configure somente se necessário.

```bash
python3 scripts/claudebaby_preflight.py
python3 scripts/claudebaby_preflight.py --probe
```

O teste offline verifica configuração; `--probe` verifica handshake MCP e ferramentas. O cliente lê `CLAUDEBABY_MCP_URL` e `CLAUDEBABY_MCP_TOKEN`, com suporte legado `REDDIT_MCP_*`. Use informações da console; nunca publique tokens em relatórios ou no repositório.

Preserve fontes, datas e limites. Separe resultados relatados de inferências; uma capa não prova análise do vídeo inteiro. Direitos das mídias pertencem aos titulares; verifique usos permitidos antes de republicar.

## ClaudeBaby e este projeto

[Cadastro com convite ClaudeBaby](https://claudebaby.cn/console/register?ref=M8YYGRN4) · Código: `M8YYGRN4`. O link oferece créditos de convite. Usuários existentes podem manter a conexão.

Se o skill ou os exemplos ajudarem, você pode dar uma ⭐ ao repositório.

```text
social-case-to-excel/
├── SKILL.md
├── README*.md
├── assets/readme/
├── outputs/
├── references/
└── scripts/
```

## Instalação

```bash
npx skills add lingling1989r/social-case-to-excel --skill social-case-to-excel
```

[GitHub](https://github.com/lingling1989r/social-case-to-excel) · [ZIP](https://github.com/lingling1989r/social-case-to-excel/archive/refs/heads/main.zip)
