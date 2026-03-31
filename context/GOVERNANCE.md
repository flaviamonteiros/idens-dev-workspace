# GOVERNANCE.md — Direitos de Decisão da Área de Dev

## Princípio Central

Cada agente decide dentro do seu domínio. Fora do domínio, consulta ou escala.
Decisões reversíveis → agente decide sozinho.
Decisões irreversíveis → aprovação humana obrigatória.

---

## Direitos de Decisão por Agente

### Dev Core
✅ Decide sozinho:
- Estrutura de arquivos e pastas
- Escolha de biblioteca dentro da stack padrão
- Nomes de variáveis, funções, componentes
- Criar branches (`feat/`, `fix/`, `chore/`)
- Commits em branches de feature

⛔ Precisa de aprovação:
- Alterar a stack padrão (ex: trocar Supabase por outro banco)
- Commitar diretamente na `main`
- Deletar arquivos ou pastas
- Alterar configurações de produção

---

### Arquiteto
✅ Decide sozinho:
- Validar ou rejeitar uma abordagem técnica proposta
- Sugerir stack alternativa com justificativa
- Dividir uma tarefa grande em sub-tarefas
- Definir estrutura de dados e contratos de API

⛔ Precisa de aprovação:
- Mudanças arquiteturais que afetam múltiplos projetos
- Decisões de infraestrutura com custo financeiro
- Definir padrões novos que entrarão no GOVERNANCE.md

---

### QA / Revisor
✅ Decide sozinho:
- Aprovar ou reprovar um PR com base em qualidade
- Solicitar mudanças antes de mergear
- Criar issues para bugs encontrados

⛔ Precisa de aprovação:
- Mergear PR com ressalvas (deve sinalizar ao humano)
- Reprovar PR de alta urgência (escalar imediatamente)

---

### Deploy
✅ Decide sozinho:
- Deploy em ambiente de staging/preview
- Rollback automático em caso de falha em staging

⛔ Precisa de aprovação:
- Deploy em produção (sempre)
- Configurar variáveis de ambiente de produção
- Apontar domínio ou alterar DNS

---

### Documentador
✅ Decide sozinho:
- Gerar README, changelogs e docs técnicos
- Atualizar documentação existente com novas informações
- Registrar decisões arquiteturais (ADR)

⛔ Precisa de aprovação:
- Publicar documentação externamente (para clientes)
- Alterar documentação de contratos ou escopo de projetos

---

## Protocolo de Escalada

Quando um agente encontra uma situação fora do seu domínio:
1. Para a execução
2. Registra o bloqueio no `state.json` (blocked_tasks)
3. Notifica o humano responsável com contexto claro

Nunca assume. Nunca improvisa fora do domínio. Sempre documenta o bloqueio.

---

## Principals da Área de Dev

> ⚠️ FASE DE TESTES — qualquer um dos 3 sócios pode aprovar qualquer decisão.
> Isso permite que qualquer principal percorra e valide o fluxo completo de forma independente.
> Rever quando sair de fase de testes.

| Principal | Pode aprovar |
|-----------|-------------|
| Hugo | Qualquer decisão que requer aprovação |
| Flávia | Qualquer decisão que requer aprovação |
| Gerzi | Qualquer decisão que requer aprovação |

Conflito entre principals → reunião dos 3 antes de prosseguir.

---

## Revisão

Este documento é revisado a cada 30 dias ou quando um novo padrão precisar ser incorporado.
Última revisão: 2026-03-31
