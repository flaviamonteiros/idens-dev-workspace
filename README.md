# Idens Dev Workspace

Repositório da área de desenvolvimento da Idens.

## Estrutura

```
idens-dev-workspace/
├── agents/        ← configuração dos agentes de dev
│   ├── dev-core/      ← escreve e commita código
│   ├── arquiteto/     ← valida solução antes de codar
│   ├── qa/            ← revisa código antes de mergear
│   ├── deploy/        ← gerencia ambientes e deploys
│   └── documentador/  ← gera docs e READMEs automaticamente
├── workflows/     ← fluxos de trabalho da área de dev
├── context/       ← contexto técnico da Idens (stacks, padrões, decisões)
└── projects/      ← projetos em andamento
```

## Agentes

| Agente | Função |
|--------|--------|
| Dev Core | Recebe tarefa em linguagem natural, escreve código, commita |
| Arquiteto | Valida stack, aponta riscos, define estrutura antes de codar |
| QA / Revisor | Revisa código, aponta bugs e vulnerabilidades |
| Deploy | Gerencia staging → produção |
| Documentador | Gera README, docs técnicos e registros de decisão |

## Orquestração

Um único Bot Dev (@idens_dev_bot) recebe tarefas e distribui internamente para o agente correto.
