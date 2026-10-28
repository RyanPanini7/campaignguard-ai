# CampaignGuard AI

> Aplicação web para revisar campanhas de marketing antes da publicação, combinando validações determinísticas com explicações assistidas por IA.

**Status:** planejamento / início do MVP  
**Objetivo do portfólio:** demonstrar React, TypeScript, validação de dados, HTML, integração com APIs, testes e uso responsável de IA.

## Problema que resolve

Antes de publicar uma campanha, uma pessoa precisa conferir se os dados essenciais estão preenchidos, se o link de destino está bem formado, se os parâmetros de rastreamento estão presentes e se o HTML contém problemas comuns. Fazer tudo manualmente aumenta a chance de erro.

O CampaignGuard AI reúne essas verificações em um relatório que explica os problemas e sugere próximos passos.

## Escopo do MVP

- [ ] Formulário para nome da campanha, produto, público-alvo, URL de destino e trecho HTML.
- [ ] Validações automáticas baseadas em regras claras.
- [ ] Relatório dividido em erros, alertas e sugestões.
- [ ] Interface responsiva com estados de carregamento, vazio e erro.
- [ ] Testes para as regras de validação.
- [ ] README e documentação atualizados conforme o projeto evoluir.

A IA será adicionada **depois** que as validações básicas estiverem funcionando. Ela explicará os achados e sugerirá melhorias; não substituirá as regras que determinam erros objetivos.

## Tecnologias planejadas

- React + TypeScript + Vite
- CSS inicialmente; uma biblioteca visual poderá ser adicionada depois
- Git e GitHub
- Etapa futura: servidor/API para proteger a chave do provedor de IA
- Etapa futura: testes automatizados e implantação online

## Executar localmente

Após criar o projeto React com Vite:

```bash
npm install
npm run dev
```

O terminal mostrará o endereço local para abrir no navegador.

## Estrutura de documentação

- [`docs/01-product.md`](docs/01-product.md) — problema, público, requisitos e critérios de aceite
- [`docs/02-roadmap.md`](docs/02-roadmap.md) — etapas e tarefas
- [`docs/03-architecture.md`](docs/03-architecture.md) — arquitetura prevista
- [`docs/04-test-plan.md`](docs/04-test-plan.md) — cenários de teste
- [`docs/05-decisions.md`](docs/05-decisions.md) — decisões técnicas e suas justificativas
- [`docs/06-work-log.md`](docs/06-work-log.md) — registro do que foi feito e aprendido
- [`CHANGELOG.md`](CHANGELOG.md) — alterações por versão

## Como contribuir consigo mesmo

1. Escolha uma tarefa pequena do roadmap.
2. Se necessário, crie uma branch, por exemplo `feat/campaign-form`.
3. Implemente e teste a mudança.
4. Atualize a documentação afetada.
5. Faça um commit que descreva a mudança.
6. Envie a branch ao GitHub e abra um Pull Request se estiver usando esse fluxo.

## Segurança

- Nunca coloque chaves reais de API no código do frontend ou no Git.
- Arquivos locais `.env` devem permanecer ignorados pelo Git.
- O arquivo `.env.example` deve conter somente nomes de variáveis e valores fictícios.
- A IA fornecerá recomendações; uma pessoa deverá revisar o relatório antes de tomar decisões.

## Licença

Ainda não definida. Defina uma licença antes de reutilizar ou distribuir o projeto publicamente.
