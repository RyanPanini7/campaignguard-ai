# 04 — Plano de testes

## Testes manuais iniciais

| ID | Cenário | Resultado esperado |
|---|---|---|
| MT-01 | Enviar formulário completamente vazio | Campos obrigatórios sinalizados; aplicação não quebra |
| MT-02 | Informar uma URL como `https://exemplo.com` | URL aceita pela regra de formato |
| MT-03 | Informar `ftp://exemplo.com` | URL sinalizada por protocolo não permitido |
| MT-04 | Informar uma URL malformada | Erro de URL claro |
| MT-05 | URL sem parâmetros UTM | Alerta de rastreamento exibido |
| MT-06 | HTML com `<img src="produto.png">` sem `alt` | Alerta de acessibilidade exibido |
| MT-07 | HTML com `<a href="https://exemplo.com" target="_blank">` sem `rel` | Alerta de segurança exibido |
| MT-08 | Corrigir entradas inválidas e executar de novo | Relatório é recalculado sem manter achados obsoletos |
| MT-09 | Colar HTML grande, dentro do limite estabelecido | Interface continua responsiva |
| MT-10 | Visualizar a aplicação em tela estreita | Formulário e resultados permanecem utilizáveis |

## Testes automatizados esperados

- Cada regra tem pelo menos um cenário positivo e um negativo.
- A análise combina várias regras sem descartar achados.
- Valores ausentes e strings vazias não provocam exceções.
- A ordem e a severidade dos achados permanecem previsíveis.
- O build do projeto conclui com sucesso.

## Ao integrar IA

- Simular falha/timeout do provedor.
- Simular resposta vazia, inválida ou fora do formato esperado.
- Confirmar que a tela continua mostrando as regras determinísticas mesmo se a IA falhar.
- Confirmar que conteúdo do HTML é tratado como dado, não como instrução de sistema.
- Verificar limites de tamanho e uso para evitar custos inesperados.
