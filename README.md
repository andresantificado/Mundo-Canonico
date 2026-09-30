# Mundo-Canonico

Repositório inicial de trabalho para o RPG/MMO canônico. **Ainda não existe jogo executável neste repositório. `CODEX_READY=FALSE`.**

O inventário inicial encontrou somente `.git`, sem commits, remoto ou implementação. Após essa constatação, o Criador autorizou a criação com “me ajude a criar”. A primeira entrega organiza o cânone recebido e instala verificações de integridade e de prontidão; não substitui testes do jogo.

Este primeiro commit no GitHub contém somente o README. Os documentos e as ferramentas referenciados abaixo estão na pasta local e ainda não foram enviados ao repositório remoto.

## Começar

Requisito para as verificações locais: Node.js 24. Nenhuma dependência externa é necessária nesta etapa.

```sh
node tools/verify-sources.mjs
node --test tests/governance.test.mjs
node tools/release-gate.mjs
```

O último comando deve terminar com código **1 / BLOCKED** enquanto faltarem evidências de implementação. Um gate bloqueado é o resultado correto para este estágio, não uma aprovação do produto.

## Estado e documentos

- [Checkpoint atual](docs/PHASE_0_CHECKPOINT.md).
- [Baseline antes de qualquer implementação](docs/BASELINE_REPORT.md).
- [Lacunas e bloqueios](docs/IMPLEMENTATION_GAP_REPORT.md).
- [Rastreabilidade do cânone](docs/canon/CANON_TRACEABILITY_MATRIX.md).
- [Conflitos e precedência](docs/canon/CANON_CONFLICT_REGISTER.md).
- [Plano por fases](docs/MIGRATION_PLAN_MASTER_RULESET_v1_1.md).
- [Esboço técnico da fundação](docs/adr/ADR-0001-AUTHORITATIVE_FOUNDATION.md).
- [Matriz de testes e certificação](docs/TEST_MATRIX.md).

`sources/` preserva os bytes dos documentos entregues. `.gitattributes` desativa conversão de finais de linha nessa pasta para manter os hashes após checkout. `docs/evidence/source-inventory.json` registra seus hashes SHA-256 e o inventário inicial. Os sete arquivos avulsos de Downloads são idênticos às respectivas cópias do ZIP. As duas mensagens coladas foram preservadas separadamente.

## Limites desta etapa

Não há backend, banco, migrations aplicadas, autenticação, WebSocket, interface jogável ou teste de carga executado. A arquitetura proposta mantém PostgreSQL como persistência obrigatória e separa motor genérico de conteúdo privado; ela ainda não é uma implementação.

A reconciliação integral das respostas Q1–Q300 depende dos enunciados originais, ausentes no pacote. As 44 imagens do registro visual também não foram fornecidas. Até resolver as pendências documentais, as fases de gameplay ficam bloqueadas conforme o gate do Prompt Mestre v3.

O repositório contém documentos com referências privadas. **Não o publique como pacote do `PUBLICABLE_ENGINE`.** Nenhuma licença de publicação de conteúdo de terceiros foi inferida.
