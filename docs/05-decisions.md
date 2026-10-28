# 05 — Registro de decisões técnicas

Use o formato abaixo para decisões importantes. Não precisa registrar cada detalhe pequeno; registre decisões que afetem arquitetura, segurança, custo ou manutenção.

## DEC-001 — Começar com validações determinísticas antes da IA

- **Status:** aceita
- **Contexto:** depender de IA desde o primeiro dia dificulta testar a lógica principal e pode gerar custo.
- **Decisão:** implementar as regras objetivas e a interface primeiro; acrescentar IA depois.
- **Consequências:** o MVP poderá demonstrar valor sem uma chave de API; a integração com IA ficará mais fácil de isolar e testar.

## DEC-002 — Usar React + TypeScript + Vite

- **Status:** aceita
- **Contexto:** o projeto precisa praticar React e apresentar uma configuração moderna e simples de desenvolvimento.
- **Decisão:** iniciar com o template React + TypeScript do Vite.
- **Consequências:** haverá tipagem estática; será necessário aprender os tipos gradualmente.

## Modelo para novas decisões

### DEC-XXX — Título da decisão

- **Status:** proposta / aceita / substituída
- **Contexto:** qual problema ou necessidade levou à decisão?
- **Alternativas:** quais opções foram consideradas?
- **Decisão:** o que foi escolhido e por quê?
- **Consequências:** quais benefícios, custos ou limitações surgem?
