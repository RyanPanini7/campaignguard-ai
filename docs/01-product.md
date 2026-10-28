# 01 — Definição do produto

## Visão

Ajudar profissionais de marketing e equipes técnicas a encontrar problemas comuns em uma campanha antes de ela ser publicada.

## Usuários principais

- Pessoa responsável por configurar campanhas digitais.
- Pessoa desenvolvedora ou analista que revisa HTML, links e parâmetros de rastreamento.

## Problema

A revisão manual pode deixar passar campos incompletos, URLs malformadas, parâmetros UTM ausentes e problemas básicos de acessibilidade ou segurança no HTML.

## Proposta de valor

Uma única tela que recebe os dados da campanha, executa verificações repetíveis e apresenta um relatório acionável. A IA entra como apoio para explicar os resultados em linguagem simples.

## História principal do usuário

**Como** pessoa responsável por uma campanha, **quero** informar seus dados e receber um relatório de validação, **para** corrigir problemas antes da publicação.

## Requisitos funcionais do MVP

- RF-01: permitir preencher nome da campanha, produto, público-alvo, URL de destino e HTML.
- RF-02: validar campos obrigatórios.
- RF-03: verificar se a URL pode ser interpretada e usa HTTP ou HTTPS.
- RF-04: verificar a presença de `utm_source`, `utm_medium` e `utm_campaign` na URL, apresentando ausência como alerta configurável.
- RF-05: analisar o HTML fornecido e sinalizar imagens sem `alt`.
- RF-06: sinalizar links com `target="_blank"` sem `rel="noopener noreferrer"`.
- RF-07: mostrar os achados com severidade, explicação e sugestão de correção.
- RF-08: permitir editar a campanha e rodar a análise novamente.
- RF-09: tratar entradas vazias, formatos inválidos e falhas sem quebrar a interface.

## Requisitos de qualidade

- RQ-01: interface utilizável em celular e desktop.
- RQ-02: mensagens de erro claras e sem jargões desnecessários.
- RQ-03: regras de validação separadas dos componentes visuais.
- RQ-04: testes automatizados cobrindo casos válidos e inválidos.
- RQ-05: nenhuma chave secreta exposta no código enviado ao navegador.
- RQ-06: documentação suficiente para outra pessoa instalar e testar o projeto.

## Critérios de aceite do MVP

- [ ] Uma pessoa consegue preencher os campos e executar a análise.
- [ ] Campos obrigatórios ausentes são sinalizados.
- [ ] Uma URL inválida ou com protocolo diferente de HTTP/HTTPS é sinalizada.
- [ ] Ausência de parâmetros UTM é exibida como alerta, não como falha silenciosa.
- [ ] Problemas HTML previstos nos requisitos aparecem no relatório.
- [ ] Os resultados distinguem erros de alertas.
- [ ] O usuário consegue corrigir a entrada e executar novamente.
- [ ] Os testes automatizados passam e o comando de build termina sem erro.
- [ ] README contém instruções atualizadas de instalação e execução.

## Fora do escopo da primeira versão

- Publicar ou alterar campanhas em plataformas reais.
- Fazer login, gerenciar permissões ou armazenar dados de clientes.
- Verificar de forma confiável o status de links externos ou seguir redirecionamentos.
- Executar JavaScript fornecido pelo usuário.
- Deixar a IA aprovar ou reprovar campanhas sem regras explícitas.
- Criar dashboards avançados ou análises de desempenho de campanhas.

## Métricas para avaliar o projeto

- Percentual de testes automatizados passando.
- Quantidade de regras de validação cobertas por testes.
- Tempo necessário para revisar uma campanha de exemplo.
- Número de erros e alertas identificados corretamente em um conjunto de casos de teste.
