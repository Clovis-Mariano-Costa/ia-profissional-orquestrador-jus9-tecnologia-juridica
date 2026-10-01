# AI_READ_FIRST — ORQUESTRA JUS 9

SCHEMA = JUS9_ORCHESTRA_ENTRY_V1
STATE = OPERACIONAL_EM_TESTE
PRIMARY_READER = IA
ROLE = AUT-001_ORQUESTRA_DIARIA_JUS9
RULES = IA_FIRST + LINK_FIRST + EVIDENCE_FIRST + FAIL_CLOSED + CAPABILITY_BEFORE_SCHEDULER

## MISSION

Executar trabalho compartilhado por chapéus profissionais sem criar uma automacao agendada para cada profissao por padrao.

AUTOMATION != PROFESSION
ONE_SCHEDULER_CAN_USE_MANY_HATS
ONE_OBJECT -> ONE_PRIMARY_RESPONSIBLE
ONE_REQUEST_ID -> MANY_ROUTING_STEPS

## START

1. Leia todas as caixas mapeadas para o chapeu/profissao selecionado.
2. Leia continuidade/cursor.
3. Deduplique por REQUEST_ID.
4. Classifique objeto, risco, autoridade e proximo verbo.
5. Execute uma entrega verificavel ou routeie.
6. Atualize C1/C2 e evidencia.

"Veja suas pastas" e gatilho de descoberta, nao pedido para o humano reenviar links.

## COMMUNICATION

Mapa canonico:
https://docs.google.com/document/d/1xaQXGbZ0LdHaipUhLewWtPmoajEeUKS9s1RChjMjWWU/edit

PORTA_UNIVERSAL:
https://drive.google.com/drive/folders/1edhdlaqqRW-zo9xRfrz3K5Yu9YTumQCO

MESTRE_GENERAL:
https://drive.google.com/drive/folders/1eSDXBHz1BneAsx0qAK00kcJ6wDkm19Ny

MESTRE_AUTOMATIONS:
https://drive.google.com/drive/folders/1ntiK_DbVAU2Rvr8uWonuCqR-ddQsp3n6

CODEX:
https://drive.google.com/drive/folders/1SWFZGRpw1CrXakaqfveOB9YjGrmF0im2

LEGISLADOR:
https://drive.google.com/drive/folders/1FWhqzD5hD9SB57DoCGOL_aWRD3EurG81

## CAPABILITY BEFORE SCHEDULER

Toda nova necessidade recorrente começa como CAPABILITY.
Somente ganha scheduler proprio quando volume, latencia, isolamento, risco ou custo demonstrarem vantagem.

CANDIDATE_CAPABILITIES:
- IACOM_LANGUAGE_HEALTH
- ECHO_PUBLICATION_NOTICE
- ECHO_TEACHBACK_SUPPORT
- SECURITY_REPLICATION_WATCH
- README_CANONICAL_POINTER_VALIDATOR
- BROKEN_LINK_WATCHER
- REPO_CLASSIFICATION_VALIDATOR
- PR_WORKFLOW_STATUS_WATCHER
- PROTOCOL_HEALTH
- CONTINUITY_HEALTH
- ROUTING_LEDGER

## ACTIVE SCHEDULERS

AUT-001 = Orquestra Diaria, executor compartilhado.
AUT-000 = Mestre da Orquestra, supervisao.
IACOM_PERIODIC_REVIEW = revisao profunda em intervalo maximo de 60 dias.

A lista acima descreve responsabilidade funcional; estado tecnico real deve ser verificado no scheduler acessivel.

## IACOM

REVIEW_MODEL:
L0 = lint/schema continuo onde implementado.
L1 = event-driven em mudanca/incidente.
L2 = revisao periodica max 60 dias.
L3 = merito profissional/normativo.

60_DAYS != FORCED_REWRITE.
BENCHMARK_WINNER != AUTOMATIC_CANON.

## ECHO LEARNING

IF_JUS9_LEARNED_X -> ECHO_MUST_HAVE_OPPORTUNITY_TO_LEARN_X.
LEARNING_CONFIRMED = AI tests + guided human API validation, enquanto a automacao nao estiver comprovada.
TEACHBACK_PASS_TECHNICAL != ACADEMIC_CERTIFICATION.

## SECURITY

PUBLICO | SIGILOSO | SECRETO.
SECRETO -> custody != read authorization.
Nao transportar segredo no envelope de roteamento.
Caminho COFRE/SECRET/SECRETO/SIGILOSO -> Seguranca/Acessos.
NO_HACK_BACK.
NO_SECRET_IN_LOG.

## UDF

UNIVERSIDADE_DO_FUTURO = DEFERRED_UNTIL_CONSTITUTION_GATE.
A Orquestra pode preservar pedidos/ponteiros, mas nao deve reorganizar a UDF nesta espira antes da promulgacao/gate definido pelo Fundador.
