# 03 — Arquitetura prevista

## Princípios

1. Começar simples e evoluir conforme houver necessidade.
2. Manter as regras de negócio separadas da interface React.
3. A análise objetiva deve funcionar mesmo sem IA.
4. Não confiar em conteúdo fornecido pelo usuário como código executável.
5. Não expor credenciais no frontend.

## Arquitetura por etapas

### Etapa inicial: frontend

- React + TypeScript + Vite.
- Formulário e relatório executados no navegador.
- Funções puras de validação em um módulo separado.
- Sem banco de dados e sem integração com IA nesta etapa.

### Etapa de IA: servidor

- Adicionar um servidor/API separado, por exemplo com Node.js.
- O frontend envia os dados necessários ao endpoint do servidor.
- O servidor lê a chave da IA de uma variável de ambiente.
- O servidor envia ao modelo os achados objetivos e solicita explicações/sugestões estruturadas.
- O servidor valida e limita a resposta antes de enviá-la ao frontend.

## Estrutura de pastas desejada

A estrutura real deve acompanhar o crescimento do projeto. Não crie todas as pastas antes de precisar delas.

```text
campaignguard-ai/
├── .github/
│   └── ISSUE_TEMPLATE/
├── docs/
├── src/
│   ├── components/
│   ├── features/
│   │   └── campaign-validation/
│   ├── types/
│   ├── utils/
│   ├── App.tsx
│   └── main.tsx
├── public/
├── .env.example
├── .gitignore
├── CHANGELOG.md
├── README.md
└── package.json
```

Se for adicionado um servidor, documente a nova estrutura antes de espalhar lógica de servidor pelo frontend.

## Modelo inicial de dados

### CampaignInput

- `campaignName`: string
- `product`: string
- `audience`: string
- `destinationUrl`: string
- `htmlContent`: string

### ValidationFinding

- `id`: identificador estável
- `ruleId`: identificador da regra, por exemplo `URL_INVALID`
- `severity`: `error`, `warning` ou `info`
- `title`: resumo curto
- `message`: descrição do problema
- `suggestion`: ação recomendada
- `source`: `rule` ou `ai`

A resposta da IA não deve poder apagar ou alterar os achados determinísticos; deve complementá-los.

## Segurança e limites

- Tratar a URL como texto fornecido pelo usuário; não fazer requisições arbitrárias a URLs na primeira versão.
- Analisar HTML sem executá-lo.
- Escapar ou sanitizar conteúdo exibido na interface quando necessário.
- Aplicar limite de tamanho para campos e conteúdo HTML.
- Nunca inserir uma chave de API em variáveis `VITE_*`, pois variáveis prefixadas dessa forma ficam disponíveis no bundle do frontend.
- Antes de adicionar persistência ou serviço de IA, documentar quais dados são enviados e para onde.
