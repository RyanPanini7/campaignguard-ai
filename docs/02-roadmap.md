# 02 — Roadmap e tarefas

Use caixas de seleção para atualizar o progresso. Para tarefas maiores, crie Issues no GitHub e coloque o número da Issue aqui.

## Fase 0 — Preparação

- [ ] P0-01 Criar repositório local e remoto.
- [ ] P0-02 Adicionar README e documentos de planejamento.
- [ ] P0-03 Registrar o primeiro commit de documentação.
- [ ] P0-04 Criar projeto React + TypeScript com Vite.
- [ ] P0-05 Confirmar que `npm run dev` e `npm run build` funcionam.

## Fase 1 — Interface e fluxo principal

- [ ] P1-01 Remover conteúdo de demonstração do template.
- [ ] P1-02 Criar layout responsivo do CampaignGuard AI.
- [ ] P1-03 Criar formulário da campanha.
- [ ] P1-04 Criar botão para executar análise.
- [ ] P1-05 Criar componentes para exibir erros, alertas e sugestões.
- [ ] P1-06 Implementar estados vazio, carregando e erro.

## Fase 2 — Regras de validação sem IA

- [ ] P2-01 Criar tipos TypeScript para campanha e achado de validação.
- [ ] P2-02 Implementar validação de campos obrigatórios.
- [ ] P2-03 Implementar validação da URL e do protocolo.
- [ ] P2-04 Implementar verificação dos parâmetros UTM.
- [ ] P2-05 Implementar verificação de imagens sem `alt`.
- [ ] P2-06 Implementar verificação de `target="_blank"` sem `rel` seguro.
- [ ] P2-07 Integrar regras ao relatório da interface.
- [ ] P2-08 Adicionar testes automatizados para cada regra.

## Fase 3 — Qualidade e apresentação

- [ ] P3-01 Melhorar acessibilidade e navegação por teclado.
- [ ] P3-02 Testar os principais tamanhos de tela.
- [ ] P3-03 Adicionar exemplos de campanhas para demonstração.
- [ ] P3-04 Revisar textos, mensagens e tratamento de erros.
- [ ] P3-05 Atualizar README com imagens ou GIF da aplicação.
- [ ] P3-06 Fazer build de produção e revisar avisos.

## Fase 4 — Integração com IA (após o MVP funcionar)

- [ ] P4-01 Escolher um provedor e revisar preço, limites e política de dados.
- [ ] P4-02 Criar endpoint no servidor para chamar o modelo.
- [ ] P4-03 Guardar a chave em variável de ambiente no servidor.
- [ ] P4-04 Enviar somente os dados necessários para explicar os achados.
- [ ] P4-05 Exigir resposta estruturada e validar o formato retornado.
- [ ] P4-06 Exibir as explicações geradas pela IA separadas dos resultados objetivos.
- [ ] P4-07 Tratar timeouts, limites de uso e respostas inválidas.
- [ ] P4-08 Documentar limitações e testar casos adversariais.

## Fase 5 — Publicação

- [ ] P5-01 Escolher hospedagem para frontend e servidor.
- [ ] P5-02 Configurar variáveis de ambiente no ambiente publicado.
- [ ] P5-03 Publicar demonstração online.
- [ ] P5-04 Adicionar link da demonstração e do repositório ao currículo/portfólio.

## Definição de pronto

Uma tarefa está pronta quando o comportamento esperado funciona, os casos relevantes foram testados, os nomes estão claros, a documentação afetada foi atualizada e as alterações foram registradas em um commit.
