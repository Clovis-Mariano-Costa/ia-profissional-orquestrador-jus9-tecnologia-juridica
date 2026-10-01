# IA READ FIRST — ORQUESTRADOR JUS 9

SCHEMA = JUS9_REPO_ENTRY_V1
STATE = DRAFT_BRANCH
PRIMARY_READER = IA
CLASSIFICATION = PUBLICO_SANITIZADO
RULES = IA_FIRST + LINK_FIRST + EVIDENCE_FIRST + FAIL_CLOSED

## PURPOSE
Arquitetura tecnica de orquestracao.
AUT-001 Orquestra Diaria = executor compartilhado por chapeus.
AUT-000 Mestre = supervisao, prioridade, conflito e AgentRouter logico.

COMMUNICATION_MAP = https://docs.google.com/document/d/1xaQXGbZ0LdHaipUhLewWtPmoajEeUKS9s1RChjMjWWU/edit
GITHUB_INVENTORY = https://docs.google.com/document/d/1MfktKZtfL9imoyZ9DWDmBe3-z2jE_2HkRcTXydPSrPI/edit

## REQUEST FLOW
DISCOVER -> READ_ALL_MAPPED_INBOXES -> DEDUP_REQUEST_ID -> CLASSIFY -> RESPONSIBLE_PRIMARY -> COLLABORATORS -> EXECUTE -> EVIDENCE -> C1/C2

ONE_OBJECT = ONE_REQUEST_ID
MULTIPLE_INBOXES != DUPLICATION
ONE_BOX_EMPTY != NO_PENDING_REQUESTS
HUMAN_LINK_COURIER_REQUIRED = FALSE

## AUTOMATION
AUTOMATE_MECHANICAL = YES
AUTOMATE_RESERVED_MERIT = NO
NEW_SCHEDULER = only when volume/frequency/latency/isolation justify it
PREFER_SHARED_ORCHESTRA = TRUE

## SECURITY
Never carry raw secrets in routing envelopes.
PUBLICO/SIGILOSO/SECRETO classification must be preserved.
SECRETO -> metadata only unless current authorization permits content access.

## NEXT
Reconcile AgentRouter + CompetenceRegistry + ledger + C0/C1/C2 + IACOM review, preserving dry-run and rollback.
