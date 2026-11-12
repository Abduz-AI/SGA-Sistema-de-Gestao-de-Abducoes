# Backlog — SGA / Abduz-AI

**Versão 1.0 — 01/10/2026**

7 épicos · 16 features · 30 histórias · 98 critérios de aceitação.

As prioridades Alta/Média são propostas de organização, sem sprints, estimativas ou responsáveis inventados. Ready significa cenário descrito para revisão; Refining indica lacuna associada. Os cartões do Project representam essas histórias.

## Hierarquia e visão geral

| Epic | Feature | Histórias |
|---|---|---|
| EPIC-001 — Humanos e pesquisa | FEAT-001 — Cadastro de humanos | [US-001](#us-001) |
| EPIC-001 — Humanos e pesquisa | FEAT-002 — Pesquisa e avaliação pré-missão | [US-002](#us-002), [US-003](#us-003) |
| EPIC-002 — Frota e deslocamento | FEAT-003 — Cadastro e situação da nave | [US-004](#us-004) |
| EPIC-002 — Frota e deslocamento | FEAT-004 — Percurso e autonomia | [US-005](#us-005) |
| EPIC-003 — Planejamento e execução de missões | FEAT-005 — Composição e validação do agendamento | [US-006](#us-006), [US-007](#us-007) |
| EPIC-003 — Planejamento e execução de missões | FEAT-006 — Ciclo de vida da missão | [US-008](#us-008), [US-009](#us-009), [US-010](#us-010), [US-011](#us-011) |
| EPIC-003 — Planejamento e execução de missões | FEAT-007 — Notificação dos envolvidos | [US-012](#us-012) |
| EPIC-004 — Funcionários e controle de acesso | FEAT-008 — Ciclo cadastral dos funcionários | [US-013](#us-013), [US-014](#us-014) |
| EPIC-004 — Funcionários e controle de acesso | FEAT-009 — Autenticação e credenciais | [US-015](#us-015), [US-016](#us-016), [US-017](#us-017), [US-018](#us-018) |
| EPIC-005 — Retornos e tratamento de ocorrências | FEAT-010 — Retorno e relato | [US-019](#us-019) |
| EPIC-005 — Retornos e tratamento de ocorrências | FEAT-011 — Advertências e correção | [US-020](#us-020), [US-021](#us-021) |
| EPIC-005 — Retornos e tratamento de ocorrências | FEAT-012 — Análise de morte | [US-022](#us-022), [US-023](#us-023) |
| EPIC-006 — Pesquisa científica | FEAT-013 — Coleta, manutenção e consulta | [US-024](#us-024) |
| EPIC-006 — Pesquisa científica | FEAT-014 — Obsolescência científica | [US-025](#us-025) |
| EPIC-007 — Histórico e auditoria | FEAT-015 — Consulta e correção do histórico | [US-026](#us-026), [US-027](#us-027) |
| EPIC-007 — Histórico e auditoria | FEAT-016 — Trilhas de acesso, alteração e consulta | [US-028](#us-028), [US-029](#us-029), [US-030](#us-030) |

## Dependências importantes

Cadastros de humanos, naves e funcionários sustentam pesquisa e planejamento. Agendamento requer pesquisa, capacidade, autonomia e disponibilidade. Retorno, conclusão e ocorrências dependem da execução. Cientistas registram dados após a abdução. Autenticação e auditoria são condições transversais, não uma ordem de codificação.

## Questões ainda abertas

Há 33 registros OPEN herdados: OPEN-015 já tem resolução terminológica, OPEN-010 não autoriza novos estados científicos e os demais preservam limites de refinamento. As mais impactantes tratam de horários/conflitos, transições, múltiplos humanos, permissões, punições e retenção/exclusão. [Ver registro completo](DISCOVERY-SGA.md#14-questões-abertas).

<a id="us-001"></a>
## US-001 — Cadastrar e consultar humanos

**ID:** US-001
**Epic:** EPIC-001 — Humanos e pesquisa
**Feature:** FEAT-001 — Cadastro de humanos
**Objetivo:** Manter a identificação dos humanos pesquisados e participantes das missões.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Evita dispersão dos dados usados na pesquisa e no planejamento.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero manter o cadastro de humanos, para identificar os participantes das missões.

## Descrição detalhada

Manter a identificação dos humanos pesquisados e participantes das missões. Humano, nome, localização, idade e popularidade. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Gestor/Supervisor autenticado; para consulta, humano já cadastrado.

## Fluxo principal

1. Informar nome, localização, idade e popularidade.
2. Registrar o cadastro do humano.
3. Consultar os dados registrados para uso na pesquisa.

## Fluxos alternativos

Consultar cadastro existente em vez de criar outro.

## Exceções

Validações de campos e duplicidade dependem de OPEN-023.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-028:** Permitir cadastrar e consultar humanos.
- **FR-029:** Manter no cadastro do humano nome, localização, idade e popularidade.

## Validações

Nome, localização, idade e popularidade devem ser mantidos; obrigatoriedade e escala de popularidade não definidas.

## Dados envolvidos

Humano, nome, localização, idade e popularidade.

## Dependências

Sem outra história predecessora de domínio identificada. Autenticação/permissão continua aplicável quando indicada na pré-condição.

## Critérios de aceitação

- [ ] **AC-001** — Quando um humano for cadastrado, então nome, localização, idade e popularidade são mantidos no cadastro.
- [ ] **AC-002** — Dado um humano cadastrado, quando consultá-lo, então seus dados cadastrados são apresentados.

## Observações e questões abertas

- Identificador único, obrigatoriedade e escalas de popularidade dependem de definição. Humano é participante do domínio, não usuário do SGA.
- **OPEN-023:** Definir validações dos dados cadastrais e científicos.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-002 → **Requisitos:** FR-028, FR-029 → **Regras:** condições dos FR → **História:** US-001 → **Aceitação:** AC-001, AC-002.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-002"></a>
## US-002 — Registrar pesquisa antes da missão

**ID:** US-002
**Epic:** EPIC-001 — Humanos e pesquisa
**Feature:** FEAT-002 — Pesquisa e avaliação pré-missão
**Objetivo:** Reunir informações de vida e localização antes do agendamento.
**Ator:** Pesquisador
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Sustenta a avaliação humana e reduz missões sem informação prévia.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Pesquisador, quero registrar informações de vida e de localização, para fornecer dados à avaliação da missão.

## Descrição detalhada

Reunir informações de vida e localização antes do agendamento. Idade, patrimônio/riqueza, emprego, fonte de renda, popularidade, interações sociais, informações gerais e locais pesquisados. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Pesquisador autenticado; humano identificado.

## Fluxo principal

1. Selecionar o humano pesquisado.
2. Registrar dados de vida e informações dos locais.
3. Disponibilizar a pesquisa para avaliação administrativa.

## Fluxos alternativos

Registrar diferentes locais pesquisados para apoiar a escolha humana.

## Exceções

Missão sem pesquisa não pode ser agendada; suficiência da pesquisa coletiva está em OPEN-025.

## Regras de negócio relacionadas

- **BR-009:** Pesquisa pré-missão é obrigatória antes do agendamento.

## Requisitos relacionados

- **FR-031:** Exigir pesquisa pré-missão antes do agendamento de toda missão.
- **FR-032:** Permitir ao Pesquisador registrar pesquisa sobre idade, patrimônio/riqueza, emprego, fonte de renda, popularidade, interações sociais e informações gerais da vida.
- **FR-033:** Permitir ao Pesquisador registrar pesquisa de localização para identificar locais mais calmos.

## Validações

Presença de pesquisa antes do agendamento; não automatizar a classificação de locais calmos.

## Dados envolvidos

Idade, patrimônio/riqueza, emprego, fonte de renda, popularidade, interações sociais, informações gerais e locais pesquisados.

## Dependências

- US-001 — Cadastrar e consultar humanos

## Critérios de aceitação

- [ ] **AC-003** — Quando o Pesquisador registrar a pesquisa, então pode registrar todos os grupos de informações previstos em FR-032.
- [ ] **AC-004** — Quando registrar informações de localização, então elas ficam disponíveis para identificar locais mais calmos na avaliação humana.
- [ ] **AC-005** — Dada uma missão sem pesquisa pré-missão, quando tentar agendá-la, então o agendamento é impedido.

## Observações e questões abertas

- Não criar pontuação automática de tranquilidade nem estados adicionais da pesquisa. Completude por humano em missão coletiva depende de OPEN-025.
- **OPEN-011:** O levantamento não definiu fórmula/critério para calcular “locais mais calmos” na pesquisa pré-missão.
- **OPEN-025:** Definir suficiência da pesquisa em missões com vários humanos.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-002 → **Requisitos:** FR-031, FR-032, FR-033 → **Regras:** BR-009 → **História:** US-002 → **Aceitação:** AC-003, AC-004, AC-005.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-003"></a>
## US-003 — Avaliar pesquisa e autorizar prosseguimento

**ID:** US-003
**Epic:** EPIC-001 — Humanos e pesquisa
**Feature:** FEAT-002 — Pesquisa e avaliação pré-missão
**Objetivo:** Decidir se a missão pode continuar após a pesquisa.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Impede prosseguimento quando a avaliação identifica relevância global.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero avaliar a pesquisa com o Supervisor, para decidir se a missão pode prosseguir.

## Descrição detalhada

Decidir se a missão pode continuar após a pesquisa. Pesquisa, avaliação humana, relevância global e decisão. DEC-002 distingue ocorrências durante/depois da missão. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Pesquisa disponível; Gestor/Supervisor autenticado.

## Fluxo principal

1. Consultar a pesquisa pré-missão.
2. Avaliar humanamente as informações e eventuais impedimentos.
3. Na ausência de impedimento, o Gestor decide se a missão prossegue.

## Fluxos alternativos

Quando identificada relevância global, registrar cancelamento definitivo.

## Exceções

Relevância global impede prosseguimento; não confundir morte/retorno inadequado com exceção pré-missão.

## Regras de negócio relacionadas

- **BR-010:** A avaliação de exceções é humana, realizada por Gestor e Supervisor.
- **BR-011:** Relevância global impede a prossecução da missão e resulta em cancelamento definitivo.

## Requisitos relacionados

- **FR-034:** Permitir que Gestor e Supervisor avaliem as informações da pesquisa.
- **FR-035:** Não realizar automaticamente a classificação de exceções; a identificação cabe à avaliação humana de Gestor/Supervisor.
- **FR-036:** Impedir a prossecução da missão quando for identificada relevância em escala global, resultando em cancelamento definitivo.
- **FR-037:** Quando não houver exceção relevante para impedir a missão, permitir que o Gestor decida se a abdução prosseguirá.

## Validações

Classificação humana; decisão de cancelamento definitiva.

## Dados envolvidos

Pesquisa, avaliação humana, relevância global e decisão. DEC-002 distingue ocorrências durante/depois da missão.

## Dependências

- US-002 — Registrar pesquisa antes da missão

## Critérios de aceitação

- [ ] **AC-006** — Dada uma pesquisa registrada, então Gestor e Supervisor podem avaliar suas informações.
- [ ] **AC-007** *(condicionado ao refinamento indicado)* — Quando uma exceção for classificada, então a identificação decorre da avaliação humana, não de classificação automática do SGA.
- [ ] **AC-008** — Dada relevância global identificada, então a missão não prossegue e seu cancelamento é definitivo.
- [ ] **AC-009** — Dada ausência de impedimento relevante, então o Gestor pode decidir pelo prosseguimento.

## Observações e questões abertas

- O momento de criação do registro cancelável e o efeito de um humano com relevância global em missão com vários humanos estão pendentes.
- **OPEN-026:** Definir cancelamento por relevância global antes do agendamento.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-002 → **Requisitos:** FR-034, FR-035, FR-036, FR-037 → **Regras:** BR-010, BR-011 → **História:** US-003 → **Aceitação:** AC-006, AC-007, AC-008, AC-009.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-004"></a>
## US-004 — Manter cadastro e manutenção das naves

**ID:** US-004
**Epic:** EPIC-002 — Frota e deslocamento
**Feature:** FEAT-003 — Cadastro e situação da nave
**Objetivo:** Manter capacidade, autonomia e situação operacional da frota.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Evita planejamento com informações incorretas ou nave em manutenção.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero cadastrar naves e controlar sua situação operacional, para planejar missões sem utilizar naves em manutenção.

## Descrição detalhada

Manter capacidade, autonomia e situação operacional da frota. Nave, capacidade total, quilômetros que pode voar e status operacional. Nave e status disponível/manutenção. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Gestor/Supervisor autenticado; nave existente para alteração.

## Fluxo principal

1. Cadastrar capacidade total, quilômetros disponíveis e status da nave.
2. Consultar os dados para planejar missões.
3. Alterar status entre disponível e manutenção quando necessário.

## Fluxos alternativos

Atualizar dados de nave já cadastrada.

## Exceções

Nave em manutenção não pode participar de missão; efeito em missões existentes em OPEN-019.

## Regras de negócio relacionadas

- **BR-001:** Gestor e Supervisor possuem poderes iguais no sistema.
- **BR-004:** Nave em manutenção não pode participar de missão.

## Requisitos relacionados

- **FR-019:** Permitir cadastrar e alterar dados de naves.
- **FR-020:** Manter para a nave os dados definidos: capacidade total, quilômetros que pode voar e status operacional.
- **FR-021:** Permitir alterar o status operacional entre disponível e manutenção pelo Gestor ou Supervisor.
- **FR-022:** Impedir a utilização de nave em manutenção em uma missão.

## Validações

Capacidade e autonomia cadastradas; manutenção impede uso; limites dos campos em OPEN-023.

## Dados envolvidos

Nave, capacidade total, quilômetros que pode voar e status operacional.

Nave e status disponível/manutenção.

## Dependências

Sem outra história predecessora de domínio identificada. Autenticação/permissão continua aplicável quando indicada na pré-condição.

## Critérios de aceitação

- [ ] **AC-010** — Quando Gestor/Supervisor cadastrar uma nave, então o cadastro mantém capacidade total, quilômetros disponíveis e status operacional.
- [ ] **AC-011** — Dada uma nave cadastrada, quando seus dados forem alterados, então os valores atualizados são apresentados para planejamento.
- [ ] **AC-012** — Dada uma nave, quando Gestor/Supervisor alterar o status, então ele pode assumir disponível ou manutenção.
- [ ] **AC-013** — Dada uma nave em manutenção, quando for utilizada na definição/agendamento de missão, então o uso é impedido.

## Observações e questões abertas

- Identificador, obrigatoriedade e limites numéricos dos campos não estão definidos.
- Tratamento das missões já agendadas quando a nave entra em manutenção não está definido.
- **OPEN-019:** Tratar indisponibilidade surgida depois do agendamento.
- **OPEN-023:** Definir validações dos dados cadastrais e científicos.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-003 → **Requisitos:** FR-019, FR-020, FR-021, FR-022 → **Regras:** BR-001, BR-004 → **História:** US-004 → **Aceitação:** AC-010, AC-011, AC-012, AC-013.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-005"></a>
## US-005 — Validar percurso e autonomia

**ID:** US-005
**Epic:** EPIC-002 — Frota e deslocamento
**Feature:** FEAT-004 — Percurso e autonomia
**Objetivo:** Comparar a autonomia com o percurso completo de ida e volta.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Evita planejar deslocamento sem autonomia para retorno.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero verificar a autonomia para todo o percurso, para planejar uma missão com retorno ao Estacionamento Alien.

## Descrição detalhada

Comparar a autonomia com o percurso completo de ida e volta. Autonomia em quilômetros, distância total, origem e retorno no Estacionamento Alien. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Nave cadastrada; percurso total e autonomia informados/obtidos conforme critério ainda a detalhar.

## Fluxo principal

1. Considerar saída do Estacionamento Alien.
2. Considerar deslocamento ao local da missão e retorno ao Estacionamento Alien.
3. Comparar distância total com a autonomia cadastrada.

## Fluxos alternativos

Selecionar outra nave ou rever o planejamento após insuficiência; a forma de revisão não cria nova regra.

## Exceções

Autonomia insuficiente não satisfaz a validação de agendamento.

## Regras de negócio relacionadas

- **BR-016:** Nave parte e retorna ao Estacionamento Alien.
- **BR-017:** Autonomia considera o percurso completo de ida e retorno.

## Requisitos relacionados

- **FR-025:** Considerar o Estacionamento Alien como ponto de partida das naves.
- **FR-026:** Considerar o Estacionamento Alien como destino de retorno das naves.
- **FR-027:** Verificar a autonomia da nave para o percurso completo da missão, incluindo ida e retorno.

## Validações

Incluir ida e volta; obtenção da distância e limite de igualdade em OPEN-009/024.

## Dados envolvidos

Autonomia em quilômetros, distância total, origem e retorno no Estacionamento Alien.

## Dependências

- US-004 — Manter cadastro e manutenção das naves

## Critérios de aceitação

- [ ] **AC-014** — Dado um percurso de missão, então sua origem e seu destino de retorno são o Estacionamento Alien.
- [ ] **AC-015** — Dadas distância total e autonomia conhecidas, quando validar o percurso, então a comparação considera ida e retorno.
- [ ] **AC-016** — Dada autonomia inferior à distância total, então a validação aponta insuficiência; a regra para satisfazer todas as validações do agendamento permanece aplicável.

## Observações e questões abertas

- O percurso está decidido (DEC-005); origem da distância, medição e fronteira de autonomia exatamente igual dependem de refinamento.
- **OPEN-009:** O levantamento não definiu como medir quilometragem/autonomia da nave nem a unidade/critério operacional além do valor cadastrado.
- **OPEN-024:** Definir fronteiras temporais e numéricas do agendamento.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-003 → **Requisitos:** FR-025, FR-026, FR-027 → **Regras:** BR-016, BR-017 → **História:** US-005 → **Aceitação:** AC-014, AC-015, AC-016.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-006"></a>
## US-006 — Definir missão, tripulação e capacidade

**ID:** US-006
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-005 — Composição e validação do agendamento
**Objetivo:** Preparar uma missão com recursos e lotação adequados.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Centraliza o planejamento e impede excesso de ocupantes.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero definir a missão e validar sua tripulação e capacidade, para preparar um agendamento com recursos adequados.

## Descrição detalhada

Preparar uma missão com recursos e lotação adequados. Humano(s), nave, tripulação, local, data, horário e intervalo da missão. Capacidade total, quantidade de tripulantes e humanos. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Gestor autenticado; humanos, funcionários e nave cadastrados; pesquisa e decisão de prosseguimento disponíveis.

## Fluxo principal

1. Registrar solicitação com humano(s), nave, local, data e horário.
2. Selecionar tripulação ativa e disponível com Piloto e Abduzidor.
3. Somar tripulantes e humanos e comparar com a capacidade.
4. Encaminhar o planejamento para as demais validações de agendamento.

## Fluxos alternativos

Incluir mais de um humano quando a capacidade comportar.

## Exceções

Tripulação mínima ausente, funcionário inativo ou capacidade excedida impedem planejamento válido.

## Regras de negócio relacionadas

- **BR-002:** Funcionário inativo não pode ser selecionado para nova missão.
- **BR-005:** Capacidade da nave inclui tripulação e humanos.
- **BR-006:** Uma missão exige pelo menos um Piloto e um Abduzidor.

## Requisitos relacionados

- **FR-038:** Permitir ao Gestor definir humano, nave, tripulação, local, data e horário da missão.
- **FR-039:** Permitir ao Gestor iniciar/registrar a solicitação da missão.
- **FR-043:** Exigir pelo menos um Piloto e um Abduzidor na tripulação.
- **FR-044:** Considerar apenas funcionários ativos e disponíveis na seleção da tripulação.
- **FR-045:** Considerar tripulação e humanos no cálculo da capacidade da nave.
- **FR-046:** Permitir mais de um humano na mesma missão, desde que respeitada a capacidade da nave.
- **FR-047:** Bloquear agendamento quando a capacidade da nave for excedida.

## Validações

Pelo menos um Piloto e um Abduzidor; ocupantes incluem tripulação e humanos; soma não pode exceder capacidade.

## Dados envolvidos

Humano(s), nave, tripulação, local, data, horário e intervalo da missão.

Capacidade total, quantidade de tripulantes e humanos.

## Dependências

- US-001 — Cadastrar e consultar humanos
- US-003 — Avaliar pesquisa e autorizar prosseguimento
- US-004 — Manter cadastro e manutenção das naves
- US-013 — Administrar cadastro de funcionários

## Critérios de aceitação

- [ ] **AC-017** — Quando o Gestor definir a missão, então registra humano(s), nave, tripulação, local, data e horário.
- [ ] **AC-018** — Dada tripulação sem Piloto ou sem Abduzidor, então a composição não satisfaz a exigência mínima.
- [ ] **AC-019** — Dada seleção da tripulação, então apenas funcionários ativos e disponíveis podem compô-la.
- [ ] **AC-020** — Dada uma nave de capacidade 4, com 2 tripulantes e 2 humanos, então a capacidade não bloqueia a missão.
- [ ] **AC-021** — Dada a mesma nave com 2 tripulantes e 3 humanos, então o agendamento é bloqueado por exceder a capacidade.
- [ ] **AC-022** — Então a contagem inclui todos os tripulantes e humanos, permitindo mais de um humano quando couber.

## Observações e questões abertas

- BR-001 concede poderes iguais ao Supervisor, enquanto vários FR citam só o Gestor; a matriz final precisa explicitar a abrangência.
- Os números são dados de teste, não limites do produto. Demais validações continuam necessárias.
- **OPEN-007:** O levantamento não definiu claramente a duração de uma missão, embora o conflito de funcionários use o intervalo entre início e término.
- **OPEN-017:** Explicitar a abrangência dos poderes iguais de Gestor e Supervisor.
- **OPEN-023:** Definir validações dos dados cadastrais e científicos.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-038, FR-039, FR-043, FR-044, FR-045, FR-046, FR-047 → **Regras:** BR-002, BR-005, BR-006 → **História:** US-006 → **Aceitação:** AC-017, AC-018, AC-019, AC-020, AC-021, AC-022.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-007"></a>
## US-007 — Impedir conflitos no agendamento

**ID:** US-007
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-005 — Composição e validação do agendamento
**Objetivo:** Verificar disponibilidade e sobreposição de recursos.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Evita alocação simultânea incompatível de pessoas e naves.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero verificar disponibilidade e sobreposição, para evitar alocar os mesmos recursos em missões incompatíveis.

## Descrição detalhada

Verificar disponibilidade e sobreposição de recursos. Nave, funcionários, humanos e intervalos de missão. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão definida com recursos; intervalos das missões disponíveis.

## Fluxo principal

1. Verificar disponibilidade da nave e dos funcionários.
2. Comparar os intervalos dos funcionários e humanos com outras missões.
3. Permitir agendamento Pendente apenas quando todas as validações forem satisfeitas.

## Fluxos alternativos

Corrigir recursos ou horário antes de nova tentativa, mantendo as validações.

## Exceções

Bloquear agendamento com recurso indisponível, funcionário sobreposto ou humano em missão simultânea.

## Regras de negócio relacionadas

- **BR-007:** Um funcionário não pode participar de missões com sobreposição de horários.
- **BR-008:** Um humano não pode participar de mais de uma missão simultaneamente.

## Requisitos relacionados

- **FR-030:** Impedir que um mesmo humano participe de mais de uma missão simultaneamente.
- **FR-040:** Verificar disponibilidade de nave e funcionários antes do agendamento.
- **FR-041:** Bloquear o agendamento quando houver conflito ou indisponibilidade.
- **FR-042:** Impedir que funcionário participe de duas missões com horários sobrepostos.

## Validações

Intervalo entre início e término; limite entre horários adjacentes e término previsto ainda em OPEN-007/024.

## Dados envolvidos

Nave, funcionários, humanos e intervalos de missão.

## Dependências

- US-006 — Definir missão, tripulação e capacidade

## Critérios de aceitação

- [ ] **AC-023** — Dado o mesmo funcionário em dois intervalos com sobreposição, quando tentar agendar a segunda missão, então o agendamento é bloqueado.
- [ ] **AC-024** — Dado um humano participante de missão simultânea, quando tentar incluí-lo em outra, então o conflito é impedido.
- [ ] **AC-025** — Dada nave ou funcionário indisponível, quando tentar agendar, então o agendamento é bloqueado.
- [ ] **AC-026** — Dadas todas as validações satisfeitas, então a missão pode ficar Pendente, conforme o fluxo consolidado.

## Observações e questões abertas

- DEC-004 define início e término como base. Falta esclarecer término previsto versus término real, fronteiras entre intervalos e disponibilidade além da situação cadastral.
- **OPEN-007:** O levantamento não definiu claramente a duração de uma missão, embora o conflito de funcionários use o intervalo entre início e término.
- **OPEN-008:** O levantamento não definiu regra operacional para determinar disponibilidade de funcionário além da condição de ativo/inativo.
- **OPEN-024:** Definir fronteiras temporais e numéricas do agendamento.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-030, FR-040, FR-041, FR-042 → **Regras:** BR-007, BR-008 → **História:** US-007 → **Aceitação:** AC-023, AC-024, AC-025, AC-026.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-008"></a>
## US-008 — Iniciar missão e registrar saída

**ID:** US-008
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-006 — Ciclo de vida da missão
**Objetivo:** Atualizar a missão no horário agendado e registrar a saída da nave.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Mantém o acompanhamento operacional coerente com o agendamento.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero acompanhar o início automático da missão, para manter o estado da missão e a saída da nave registrados.

## Descrição detalhada

Atualizar a missão no horário agendado e registrar a saída da nave. Missão Pendente, horário agendado, nave e saída. Pré-condição: agendamento validado. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão Pendente com agendamento validado.

## Fluxo principal

1. Aguardar o horário agendado.
2. Alterar automaticamente Pendente para Em andamento.
3. Registrar automaticamente a saída da nave.

## Fluxos alternativos

Missão não Pendente não é o cenário de início definido; não criar transição adicional.

## Exceções

Mudança de disponibilidade ou indisponibilidade do SGA no horário dependem de OPEN-019/027.

## Regras de negócio relacionadas

- **BR-012:** Os estados de missão são Pendente, Em andamento, Adiada, Concluída e Cancelada.

## Requisitos relacionados

- **FR-023:** Registrar automaticamente a saída da nave quando a missão entrar em Em andamento.
- **FR-048:** Manter os estados de missão: Pendente, Em andamento, Adiada, Concluída e Cancelada.
- **FR-049:** Alterar automaticamente Pendente para Em andamento no horário agendado.

## Validações

Estado de origem Pendente; horário previsto; cinco estados oficiais mantidos.

## Dados envolvidos

Missão Pendente, horário agendado, nave e saída. Pré-condição: agendamento validado.

## Dependências

- US-005 — Validar percurso e autonomia
- US-006 — Definir missão, tripulação e capacidade
- US-007 — Impedir conflitos no agendamento

## Critérios de aceitação

- [ ] **AC-027** — Dada uma missão Pendente, quando chegar o horário agendado, então seu estado muda automaticamente para Em andamento.
- [ ] **AC-028** — Quando a missão entrar em Em andamento, então a saída da nave é registrada automaticamente.
- [ ] **AC-029** — Então os estados utilizados são Pendente, Em andamento, Adiada, Concluída e Cancelada.

## Observações e questões abertas

- Fuso horário, recuperação após indisponibilidade do SGA e revalidação no instante da partida estão pendentes.
- **OPEN-019:** Tratar indisponibilidade surgida depois do agendamento.
- **OPEN-027:** Definir referência temporal e início automático após interrupção.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-023, FR-048, FR-049 → **Regras:** BR-012 → **História:** US-008 → **Aceitação:** AC-027, AC-028, AC-029.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-009"></a>
## US-009 — Concluir missão e registrar retorno da nave

**ID:** US-009
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-006 — Ciclo de vida da missão
**Objetivo:** Registrar o término informado pelo Gestor e a entrada da nave.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Fecha o ciclo normal da missão e mantém registro de retorno.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero informar o término da missão, para concluir seu registro e registrar a entrada da nave.

## Descrição detalhada

Registrar o término informado pelo Gestor e a entrada da nave. Missão, término informado e entrada da nave. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão Em andamento, conclusão normal e Gestor autenticado.

## Fluxo principal

1. Gestor informa o término da missão.
2. Sistema altera o estado para Concluída.
3. Sistema registra automaticamente a entrada da nave.

## Fluxos alternativos

Ocorrências de morte e retornos mistos seguem tratamento específico antes de fechar os critérios aplicáveis.

## Exceções

Sem definição de conclusão com morte/retornos mistos, não inferir novo status.

## Regras de negócio relacionadas

- **BR-013:** Concluída e Cancelada são estados definitivos.

## Requisitos relacionados

- **FR-024:** Registrar automaticamente a entrada da nave quando a missão passar para Concluída.
- **FR-050:** Permitir ao Gestor informar o término da missão, levando-a para Concluída.

## Validações

Concluída é definitiva; término informado e entrada automática.

## Dados envolvidos

Missão, término informado e entrada da nave.

## Dependências

- US-008 — Iniciar missão e registrar saída

## Critérios de aceitação

- [ ] **AC-030** — Dada uma missão Em andamento com conclusão normal, quando o Gestor informar o término, então ela passa para Concluída.
- [ ] **AC-031** — Quando a missão passar para Concluída, então a entrada da nave é registrada automaticamente.
- [ ] **AC-032** — Dada missão Concluída, então o estado é definitivo.

## Observações e questões abertas

- Conclusão com morte ou retornos mistos e possibilidade de nave retornada antes do fechamento administrativo não estão resolvidas.
- **OPEN-001:** Não foi definido um estado específico da missão durante a análise de morte. Não criar novo status sem decisão.
- **OPEN-018:** Definir retorno e encerramento em missões com vários humanos.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-024, FR-050 → **Regras:** BR-013 → **História:** US-009 → **Aceitação:** AC-030, AC-031, AC-032.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-010"></a>
## US-010 — Adiar missão e definir nova data

**ID:** US-010
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-006 — Ciclo de vida da missão
**Objetivo:** Permitir remarcação sem criar outro registro de missão.
**Ator:** Gestor ou Supervisor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Preserva o planejamento quando a execução é postergada.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero postergar uma missão e definir nova data, para reorganizar o planejamento mantendo o registro.

## Descrição detalhada

Permitir remarcação sem criar outro registro de missão. Missão, estado Adiada e nova data. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão existente; Gestor/Supervisor autorizado; estados de origem a confirmar.

## Fluxo principal

1. Postergar a missão e mantê-la em Adiada.
2. Aguardar nova data definida pelo Gestor/Supervisor.
3. Retornar a Pendente mantendo o mesmo registro.

## Fluxos alternativos

Enquanto não houver nova data, manter Adiada.

## Exceções

Missão Cancelada não usa este fluxo; origem e revalidação em OPEN-028.

## Regras de negócio relacionadas

- **BR-014:** Missão Adiada retorna a Pendente quando recebe nova data.

## Requisitos relacionados

- **FR-051:** Permitir postergar uma missão.
- **FR-052:** Manter missão Adiada até que Gestor ou Supervisor defina nova data.
- **FR-053:** Retornar a missão Adiada para Pendente quando nova data for definida.
- **FR-057:** Não criar um status chamado Reagendada; uma nova data de missão postergada mantém o mesmo registro e retorna a Pendente.

## Validações

Não criar estado Reagendada; não recriar registro na remarcação.

## Dados envolvidos

Missão, estado Adiada e nova data.

## Dependências

- US-006 — Definir missão, tripulação e capacidade

## Critérios de aceitação

- [ ] **AC-033** — Quando uma missão for postergada, então ela permanece em Adiada enquanto não receber nova data.
- [ ] **AC-034** — Dada missão Adiada, quando Gestor/Supervisor definir nova data, então ela retorna para Pendente mantendo o mesmo registro.
- [ ] **AC-035** — Então não se cria o estado Reagendada.

## Observações e questões abertas

- Estados de origem permitidos e revalidações na remarcação precisam ser confirmados; não tratar cancelamento como adiamento.
- **OPEN-028:** Completar transições permitidas e remarcação.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-051, FR-052, FR-053, FR-057 → **Regras:** BR-014 → **História:** US-010 → **Aceitação:** AC-033, AC-034, AC-035.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-011"></a>
## US-011 — Cancelar missão definitivamente

**ID:** US-011
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-006 — Ciclo de vida da missão
**Objetivo:** Registrar responsável e motivo do encerramento por cancelamento.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Evita reativar missões canceladas e preserva a justificativa.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero registrar cancelamento e motivo, para encerrar uma missão que não pode prosseguir.

## Descrição detalhada

Registrar responsável e motivo do encerramento por cancelamento. Missão, responsável, motivo de indisponibilidade ou exceção. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão existente; Gestor/Supervisor autorizado; estados de origem pendentes.

## Fluxo principal

1. Selecionar a missão a cancelar.
2. Registrar motivo de indisponibilidade ou exceção e responsável.
3. Alterar para Cancelada de forma definitiva.

## Fluxos alternativos

Cancelamento por relevância global segue o mesmo caráter definitivo.

## Exceções

Impedir reativação e reagendamento após cancelamento.

## Regras de negócio relacionadas

- **BR-011:** Relevância global impede a prossecução da missão e resulta em cancelamento definitivo.
- **BR-013:** Concluída e Cancelada são estados definitivos.
- **BR-015:** Cancelamento exige motivo: indisponibilidade ou exceção.

## Requisitos relacionados

- **FR-054:** Permitir cancelamento por indisponibilidade ou exceção.
- **FR-055:** Registrar quem cancelou e o motivo do cancelamento.
- **FR-056:** Considerar cancelamento definitivo, sem reativação ou reagendamento.

## Validações

Responsável e motivo registrados; indisponibilidade também gera cancelamento definitivo.

## Dados envolvidos

Missão, responsável, motivo de indisponibilidade ou exceção.

## Dependências

- US-006 — Definir missão, tripulação e capacidade

## Critérios de aceitação

- [ ] **AC-036** — Quando cancelar a missão, então o registro identifica quem cancelou e o motivo.
- [ ] **AC-037** — Dada missão Cancelada, quando tentar reativá-la ou reagendá-la, então a operação não é permitida.
- [ ] **AC-038** — Então cancelamento por indisponibilidade também é definitivo (DEC-001).

## Observações e questões abertas

- Estados a partir dos quais se pode cancelar dependem de decisão. Retorno inadequado e morte não são impedimentos da pesquisa pré-missão.
- **OPEN-026:** Definir cancelamento por relevância global antes do agendamento.
- **OPEN-028:** Completar transições permitidas e remarcação.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-054, FR-055, FR-056 → **Regras:** BR-011, BR-013, BR-015 → **História:** US-011 → **Aceitação:** AC-036, AC-037, AC-038.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-012"></a>
## US-012 — Notificar os envolvidos na missão

**ID:** US-012
**Epic:** EPIC-003 — Planejamento e execução de missões
**Feature:** FEAT-007 — Notificação dos envolvidos
**Objetivo:** Informar mudanças relevantes dentro do SGA.
**Ator:** funcionário envolvido
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Reduz desencontro de informações entre funcionários envolvidos.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como funcionário envolvido, quero receber notificações internas sobre mudanças relevantes, para acompanhar as missões de que participo.

## Descrição detalhada

Informar mudanças relevantes dentro do SGA. Missão, mudança e funcionários envolvidos. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão existente e funcionários envolvidos identificados; evento relevante a definir.

## Fluxo principal

1. Identificar mudança enquadrada no catálogo de eventos relevantes.
2. Identificar os funcionários envolvidos.
3. Disponibilizar a notificação no SGA.

## Fluxos alternativos

Mudanças não classificadas como relevantes não têm obrigação de alerta definida.

## Exceções

Falhas de entrega e troca de tripulação dependem de refinamento.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-058:** Enviar notificações internas aos funcionários envolvidos quando houver mudanças relevantes da missão.

## Validações

Canal interno para missões; não aplicar aqui o e-mail de bloqueio de login.

## Dados envolvidos

Missão, mudança e funcionários envolvidos.

## Dependências

- US-006 — Definir missão, tripulação e capacidade

## Critérios de aceitação

- [ ] **AC-039** *(condicionado ao refinamento indicado)* — Dada uma mudança classificada como relevante, quando ela ocorrer, então os funcionários envolvidos recebem notificação dentro do SGA.
- [ ] **AC-040** — Então a regra desta história usa o canal interno definido em DEC-003; e-mail de bloqueio pertence à US-016.

## Observações e questões abertas

- A lista de eventos relevantes, destinatários após troca de tripulação e prazo de entrega estão pendentes.
- **OPEN-012:** O levantamento não detalhou quais mudanças de missão são “relevantes” para disparo de notificações internas.

## Rastreabilidade

**Objetivos:** OBJ-002, OBJ-003, OBJ-004 → **Requisitos:** FR-058 → **Regras:** condições dos FR → **História:** US-012 → **Aceitação:** AC-039, AC-040.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-013"></a>
## US-013 — Administrar cadastro de funcionários

**ID:** US-013
**Epic:** EPIC-004 — Funcionários e controle de acesso
**Feature:** FEAT-008 — Ciclo cadastral dos funcionários
**Objetivo:** Cadastrar e alterar dados e credenciais iniciais dos funcionários.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Fornece a base de usuários e participantes das operações.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero manter os funcionários e suas credenciais, para administrar quem trabalha no SGA.

## Descrição detalhada

Cadastrar e alterar dados e credenciais iniciais dos funcionários. Nome, matrícula/registro, função, cargo, situação e login; senha inicial definida por Gestor/Supervisor. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Gestor/Supervisor autenticado; funcionário existente para alteração.

## Fluxo principal

1. Informar nome, matrícula/registro, função, cargo, situação e credenciais.
2. Verificar unicidade do login.
3. Registrar cadastro ou alteração do funcionário.

## Fluxos alternativos

Alterar cadastro existente sem criar novo funcionário.

## Exceções

Rejeitar login já atribuído a outro funcionário.

## Regras de negócio relacionadas

- **BR-001:** Gestor e Supervisor possuem poderes iguais no sistema.

## Requisitos relacionados

- **FR-001:** Permitir o cadastro e alteração de funcionários pelo Gestor ou Supervisor.
- **FR-006:** Garantir que o login seja único no SGA.

## Validações

Login único; campos obrigatórios e matrícula em OPEN-023.

## Dados envolvidos

Nome, matrícula/registro, função, cargo, situação e login; senha inicial definida por Gestor/Supervisor.

## Dependências

Sem outra história predecessora de domínio identificada. Autenticação/permissão continua aplicável quando indicada na pré-condição.

## Critérios de aceitação

- [ ] **AC-041** — Dado um Gestor ou Supervisor autenticado, quando cadastrar um funcionário com os dados definidos, então o funcionário e suas credenciais ficam disponíveis no cadastro.
- [ ] **AC-042** — Dado um login já cadastrado, quando tentar atribuí-lo a outro funcionário, então o cadastro não aceita a duplicação.
- [ ] **AC-043** — Dado um funcionário existente, quando Gestor/Supervisor alterar seus dados, então o cadastro apresenta os valores atualizados.

## Observações e questões abertas

- Unicidade de matrícula, campos obrigatórios e normalização de login não estão definidos.
- **OPEN-023:** Definir validações dos dados cadastrais e científicos.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-007 → **Requisitos:** FR-001, FR-006 → **Regras:** BR-001 → **História:** US-013 → **Aceitação:** AC-041, AC-042, AC-043.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-014"></a>
## US-014 — Inativar e reativar funcionários

**ID:** US-014
**Epic:** EPIC-004 — Funcionários e controle de acesso
**Feature:** FEAT-008 — Ciclo cadastral dos funcionários
**Objetivo:** Controlar situação e acesso sem excluir os registros.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Preserva histórico de pessoal e impede novos usos indevidos.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero alterar a situação do funcionário sem excluí-lo, para preservar seus registros e controlar o acesso.

## Descrição detalhada

Controlar situação e acesso sem excluir os registros. Funcionário, situação e novas credenciais na reativação (DEC-006). A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Funcionário cadastrado; Gestor/Supervisor autenticado.

## Fluxo principal

1. Selecionar o funcionário e alterar sua situação para inativo.
2. Manter o cadastro e bloquear seu acesso e seleção em novas missões.
3. Quando autorizado, reativar com novas credenciais.

## Fluxos alternativos

Reativação sem condição ou justificativa adicional, conforme a decisão herdada.

## Exceções

Efeito nas missões já agendadas precisa de OPEN-019.

## Regras de negócio relacionadas

- **BR-001:** Gestor e Supervisor possuem poderes iguais no sistema.
- **BR-002:** Funcionário inativo não pode ser selecionado para nova missão.
- **BR-003:** Funcionário inativo não é excluído do sistema e pode ser reativado pelo Gestor ou Supervisor.

## Requisitos relacionados

- **FR-002:** Manter funcionário desligado/inativo sem excluí-lo do sistema.
- **FR-003:** Impedir a seleção de funcionário inativo para novas missões.
- **FR-004:** Permitir a reativação de funcionário inativo pelo Gestor ou Supervisor, sem condição ou justificativa adicional.
- **FR-012:** Bloquear imediatamente o acesso de funcionário inativo/desligado.

## Validações

Não excluir cadastro; conta inativa não acessa; novas credenciais na reativação.

## Dados envolvidos

Funcionário, situação e novas credenciais na reativação (DEC-006).

## Dependências

- US-013 — Administrar cadastro de funcionários

## Critérios de aceitação

- [ ] **AC-044** — Dado um funcionário ativo, quando for inativado, então seu cadastro permanece e seu acesso é bloqueado.
- [ ] **AC-045** — Dado um funcionário inativo, quando forem selecionados participantes de nova missão, então ele não pode ser selecionado.
- [ ] **AC-046** — Dado um funcionário inativo, quando Gestor/Supervisor reativá-lo, então não se exige justificativa adicional e são criadas novas credenciais conforme DEC-006.

## Observações e questões abertas

- O efeito da inativação sobre missões já agendadas depende de decisão.
- **OPEN-019:** Tratar indisponibilidade surgida depois do agendamento.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-007 → **Requisitos:** FR-002, FR-003, FR-004, FR-012 → **Regras:** BR-001, BR-002, BR-003 → **História:** US-014 → **Aceitação:** AC-044, AC-045, AC-046.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-015"></a>
## US-015 — Autenticar funcionário por login e senha

**ID:** US-015
**Epic:** EPIC-004 — Funcionários e controle de acesso
**Feature:** FEAT-009 — Autenticação e credenciais
**Objetivo:** Controlar a entrada no SGA por credenciais.
**Ator:** funcionário
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Impede acesso anônimo às informações de missão.
**Status do Discovery:** Ready — cenário funcional descrito sem pendência específica bloqueante; pronto para revisão do grupo, não implementado.

## História de usuário

Como funcionário, quero entrar usando login e senha, para acessar as informações permitidas ao meu perfil.

## Descrição detalhada

Controlar a entrada no SGA por credenciais. Login, senha e situação da conta. Pré-condição: conta ativa e não bloqueada. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Conta cadastrada, ativa e sem bloqueio temporário.

## Fluxo principal

1. Funcionário informa login e senha.
2. Sistema verifica credenciais e condição da conta.
3. Concede acesso conforme o perfil quando a autenticação é válida.

## Fluxos alternativos

Credenciais inválidas resultam em acesso negado.

## Exceções

Conta inativa ou bloqueada não satisfaz as condições de acesso.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-005:** Permitir autenticação por login/usuário e senha.

## Validações

Login/senha válidos; autenticação obrigatória para dados de missão.

## Dados envolvidos

Login, senha e situação da conta. Pré-condição: conta ativa e não bloqueada.

## Dependências

- US-013 — Administrar cadastro de funcionários

## Critérios de aceitação

- [ ] **AC-047** — Dada uma conta ativa e não bloqueada, quando fornecer login e senha válidos, então a autenticação é aceita.
- [ ] **AC-048** — Dadas credenciais inválidas, quando tentar entrar, então o acesso não é concedido.
- [ ] **AC-049** — Dado um usuário não autenticado, quando tentar consultar informações de missão, então o acesso é impedido (NFR-002).

## Observações e questões abertas

- O ator é o funcionário, inclusive perfis operacionais; a tabela de FR-005 lista apenas administradores, embora a autenticação seja comum aos usuários.
- Nenhuma questão específica bloqueante vinculada; a revisão do grupo permanece necessária.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-007 → **Requisitos:** FR-005 → **Regras:** condições dos FR → **História:** US-015 → **Aceitação:** AC-047, AC-048, AC-049.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-016"></a>
## US-016 — Bloquear tentativas indevidas e alertar superiores

**ID:** US-016
**Epic:** EPIC-004 — Funcionários e controle de acesso
**Feature:** FEAT-009 — Autenticação e credenciais
**Objetivo:** Aplicar bloqueio temporário e comunicar risco de acesso indevido.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Limita tentativas consecutivas incorretas e informa os responsáveis.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero que contas com cinco erros consecutivos sejam bloqueadas e gerem alerta, para acompanhar tentativas de acesso indevido.

## Descrição detalhada

Aplicar bloqueio temporário e comunicar risco de acesso indevido. Conta, tentativas consecutivas, instante do bloqueio e aprovação de desbloqueio. Conta bloqueada, destinatários administrativos e indicação de criticidade. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Conta identificada; sequência de tentativas de senha disponível.

## Fluxo principal

1. Contabilizar cinco tentativas consecutivas de senha incorreta.
2. Bloquear a conta por quinze minutos.
3. Alertar Gestor e Supervisor no SGA e por e-mail com indicação crítica.
4. Permitir novas tentativas quando o prazo terminar.

## Fluxos alternativos

Gestor/Supervisor pode aprovar desbloqueio antes dos quinze minutos.

## Exceções

Reinício do contador, tentativas durante bloqueio e falha de e-mail estão em OPEN-020/021.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-007:** Bloquear temporariamente a conta após 5 tentativas consecutivas de senha incorreta.
- **FR-008:** Manter o bloqueio por 15 minutos ou até aprovação do Gestor/Supervisor, o que ocorrer primeiro.
- **FR-009:** Alertar imediatamente Gestor e Supervisor sobre o bloqueio por tentativas incorretas, dentro do SGA e por e-mail, indicando caráter crítico/possível risco de intrusão.

## Validações

Quinta tentativa dispara bloqueio; quatro não; desbloqueio pelo primeiro evento entre prazo e aprovação.

## Dados envolvidos

Conta, tentativas consecutivas, instante do bloqueio e aprovação de desbloqueio.

Conta bloqueada, destinatários administrativos e indicação de criticidade.

## Dependências

- US-015 — Autenticar funcionário por login e senha

## Critérios de aceitação

- [ ] **AC-050** — Dada uma conta sem falhas anteriores na sequência, quando ocorrerem quatro senhas incorretas consecutivas, então ainda não se aplica o bloqueio de cinco tentativas.
- [ ] **AC-051** — Quando ocorrer a quinta senha incorreta consecutiva, então a conta fica bloqueada.
- [ ] **AC-052** — Dada uma conta bloqueada, quando completar 15 minutos, então pode tentar autenticar novamente.
- [ ] **AC-053** — Dada uma conta bloqueada há menos de 15 minutos, quando Gestor/Supervisor aprovar o desbloqueio, então novas tentativas são permitidas antes do prazo.
- [ ] **AC-054** — Quando uma conta for bloqueada por tentativas incorretas, então o alerta é destinado a Gestor e Supervisor.
- [ ] **AC-055** — Então o alerta ocorre dentro do SGA e por e-mail, conforme FR-009.
- [ ] **AC-056** — Então a mensagem indica caráter crítico ou possível risco de intrusão.

## Observações e questões abertas

- Janela de contagem, reinício do contador e resultado de tentativas durante o bloqueio permanecem pendentes.
- O prazo mensurável de envio, endereços dos destinatários e tratamento de falhas de e-mail não foram definidos. Não confundir com notificações internas de missão.
- **OPEN-020:** Detalhar a sequência de tentativas de autenticação.
- **OPEN-021:** Detalhar alerta crítico por e-mail e dentro do SGA.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-007 → **Requisitos:** FR-007, FR-008, FR-009 → **Regras:** condições dos FR → **História:** US-016 → **Aceitação:** AC-050, AC-051, AC-052, AC-053, AC-054, AC-055, AC-056.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-017"></a>
## US-017 — Solicitar alteração ou recuperação de senha

**ID:** US-017
**Epic:** EPIC-004 — Funcionários e controle de acesso
**Feature:** FEAT-009 — Autenticação e credenciais
**Objetivo:** Condicionar mudança de senha à aprovação administrativa.
**Ator:** funcionário
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Mantém o controle definido para atualização de credenciais.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como funcionário, quero solicitar uma nova senha ao Gestor ou Supervisor, para recuperar ou atualizar meu acesso mediante aprovação.

## Descrição detalhada

Condicionar mudança de senha à aprovação administrativa. Funcionário, solicitação e aprovação administrativa. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Funcionário identificado; em esquecimento, canal externo/alternativo ainda a definir.

## Fluxo principal

1. Funcionário solicita alteração ou recuperação.
2. Gestor/Supervisor analisa a solicitação.
3. Após aprovação, permitir a alteração conforme o procedimento definido.

## Fluxos alternativos

Esquecimento de senha utiliza a mesma aprovação.

## Exceções

Sem aprovação, não permitir alteração; executor e entrega ainda pendentes.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-010:** Permitir alteração de senha somente mediante solicitação do funcionário e aprovação do Gestor ou Supervisor.
- **FR-011:** Aplicar o mesmo procedimento de aprovação para esquecimento de senha.

## Validações

Solicitação e aprovação necessárias; não presumir autoatendimento.

## Dados envolvidos

Funcionário, solicitação e aprovação administrativa.

## Dependências

- US-013 — Administrar cadastro de funcionários
- US-015 — Autenticar funcionário por login e senha

## Critérios de aceitação

- [ ] **AC-057** — Dado um funcionário que deseja alterar sua senha, quando não houver aprovação, então a alteração não é permitida.
- [ ] **AC-058** — Dada uma solicitação aprovada por Gestor/Supervisor, então a alteração de senha é permitida.
- [ ] **AC-059** — Dado esquecimento de senha, então se aplica o mesmo procedimento de solicitação e aprovação.

## Observações e questões abertas

- Canal da solicitação, executor da alteração após aprovação e entrega da nova senha estão pendentes; não presumir autoatendimento.
- **OPEN-022:** Completar o procedimento de troca e recuperação de senha.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-007 → **Requisitos:** FR-010, FR-011 → **Regras:** condições dos FR → **História:** US-017 → **Aceitação:** AC-057, AC-058, AC-059.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-018"></a>
## US-018 — Encerrar sessão ao fim do dia de trabalho

**ID:** US-018
**Epic:** EPIC-004 — Funcionários e controle de acesso
**Feature:** FEAT-009 — Autenticação e credenciais
**Objetivo:** Exigir autenticação novamente após o expediente.
**Ator:** funcionário
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Reduz continuidade de sessões além do período de trabalho definido.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como funcionário, quero ter a sessão encerrada ao final do dia de trabalho, para exigir nova autenticação no próximo acesso.

## Descrição detalhada

Exigir autenticação novamente após o expediente. Sessão e referência de final do dia de trabalho ainda não definida. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Sessão ativa; marco de fim de expediente ainda a definir.

## Fluxo principal

1. Identificar o fim do dia de trabalho conforme regra a decidir.
2. Encerrar a sessão automaticamente.
3. Exigir credenciais no próximo acesso.

## Fluxos alternativos

Não foi definido fluxo alternativo específico.

## Exceções

OPEN-005 impede determinar o instante de execução.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-013:** Encerrar automaticamente a sessão ao final do dia de trabalho; as credenciais são exigidas novamente no próximo acesso.

## Validações

Após encerramento, sessão anterior não permite novo acesso sem autenticar.

## Dados envolvidos

Sessão e referência de final do dia de trabalho ainda não definida.

## Dependências

- US-015 — Autenticar funcionário por login e senha

## Critérios de aceitação

- [ ] **AC-060** *(condicionado ao refinamento indicado)* — Dado o marco de fim do expediente definido pelo grupo, quando ele ocorrer, então a sessão é encerrada automaticamente.
- [ ] **AC-061** — Dada a sessão encerrada, quando houver novo acesso, então são exigidas credenciais novamente.

## Observações e questões abertas

- Critérios condicionados à definição do horário/regra em OPEN-005.
- **OPEN-005:** FR-013 usa “final do dia de trabalho”, mas não define horário ou regra objetiva para encerramento automático da sessão.

## Rastreabilidade

**Objetivos:** OBJ-001, OBJ-007 → **Requisitos:** FR-013 → **Regras:** condições dos FR → **História:** US-018 → **Aceitação:** AC-060, AC-061.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-019"></a>
## US-019 — Registrar retorno e ocorrências da missão

**ID:** US-019
**Epic:** EPIC-005 — Retornos e tratamento de ocorrências
**Feature:** FEAT-010 — Retorno e relato
**Objetivo:** Manter o resultado do retorno e os relatos fora do padrão.
**Ator:** Gestor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Documenta o desfecho dos humanos e subsidia tratamentos posteriores.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero registrar o resultado do retorno, para manter o desfecho da missão e suas ocorrências.

## Descrição detalhada

Manter o resultado do retorno e os relatos fora do padrão. Humano, local de abdução, local de devolução, condição de retorno e relato. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Missão em execução/retorno; Gestor autorizado a relatar.

## Fluxo principal

1. Identificar o humano e as condições do retorno.
2. Registrar retorno normal como retornado com vida ou classificar retorno inadequado.
3. Registrar relato narrativo das ocorrências no histórico.

## Fluxos alternativos

Devolução em local diferente do local de abdução gera retorno inadequado.

## Exceções

Critério de consequência de saúde e resultados diferentes na mesma missão permanecem abertos.

## Regras de negócio relacionadas

- **BR-023:** Todos os funcionários consultam o histórico; alteração é restrita a Gestor/Supervisor.

## Requisitos relacionados

- **FR-059:** Registrar retorno normal como 'retornado com vida'.
- **FR-060:** Registrar retorno inadequado quando o humano não for devolvido ao local da abdução ou sofrer consequência de saúde no retorno.
- **FR-061:** Registrar ocorrências fora do padrão no histórico da missão por meio de relato narrativo do Gestor.
- **FR-084:** Registrar no histórico as ocorrências fora do padrão.

## Validações

Comparar locais; manter relato do Gestor e resultado de retorno.

## Dados envolvidos

Humano, local de abdução, local de devolução, condição de retorno e relato.

## Dependências

- US-008 — Iniciar missão e registrar saída

## Critérios de aceitação

- [ ] **AC-062** — Dado retorno normal, quando registrá-lo, então o resultado consta como retornado com vida.
- [ ] **AC-063** — Dado humano devolvido a local diferente do local de abdução, então o retorno é registrado como inadequado.
- [ ] **AC-064** *(condicionado ao refinamento indicado)* — Dada consequência de saúde classificada como retorno inadequado, então a ocorrência é registrada; a classificação objetiva depende de OPEN-014.
- [ ] **AC-065** — Dada ocorrência fora do padrão, quando o Gestor relatá-la, então o relato narrativo fica no histórico da missão.

## Observações e questões abertas

- Retornos diferentes de humanos na mesma missão e critérios de saúde dependem de refinamento.
- **OPEN-014:** O termo “consequência de saúde” no retorno inadequado não foi operacionalizado em critérios de classificação.
- **OPEN-018:** Definir retorno e encerramento em missões com vários humanos.

## Rastreabilidade

**Objetivos:** OBJ-005 → **Requisitos:** FR-059, FR-060, FR-061, FR-084 → **Regras:** BR-023 → **História:** US-019 → **Aceitação:** AC-062, AC-063, AC-064, AC-065.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-020"></a>
## US-020 — Controlar histórico de advertências

**ID:** US-020
**Epic:** EPIC-005 — Retornos e tratamento de ocorrências
**Feature:** FEAT-011 — Advertências e correção
**Objetivo:** Manter advertências e registrar a punição prevista na quarta.
**Ator:** Gestor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Permite acompanhar reincidência por funcionário.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero registrar advertências por funcionário, para acompanhar o tratamento de retornos inadequados.

## Descrição detalhada

Manter advertências e registrar a punição prevista na quarta. Funcionário, histórico de advertências, contador normal e punição salarial. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Retorno inadequado registrado; funcionário envolvido identificado.

## Fluxo principal

1. Associar advertência ao funcionário e manter histórico.
2. Acompanhar a sequência normal de advertências.
3. Na quarta, registrar a punição salarial aplicável conforme regra definida.

## Fluxos alternativos

Advertência de cuidado por morte natural fica fora do contador normal.

## Exceções

Valor/tipo da punição, reinício e contagem por ocorrência dependem de OPEN-029.

## Regras de negócio relacionadas

- **BR-018:** Retorno inadequado gera tratamento de advertências conforme regra definida.

## Requisitos relacionados

- **FR-062:** Manter histórico de advertências por funcionário.
- **FR-063:** Aplicar três advertências para retorno inadequado e punição salarial na quarta advertência.

## Validações

Preservar histórico individual; três advertências e punição na quarta, sem desconto automático inventado.

## Dados envolvidos

Funcionário, histórico de advertências, contador normal e punição salarial.

## Dependências

- US-019 — Registrar retorno e ocorrências da missão

## Critérios de aceitação

- [ ] **AC-066** — Dado um funcionário, quando registrar advertências, então seu histórico mantém os registros associados a ele.
- [ ] **AC-067** — Dada a sequência normal de advertências por retorno inadequado, então as três primeiras são advertências e a quarta está associada à punição salarial definida no levantamento.

## Observações e questões abertas

- Valor/tipo da punição, contagem por ocorrência, responsáveis e eventual reinício do contador não estão definidos; não assumir desconto automático em folha.
- **OPEN-029:** Completar contagem de advertências e punição salarial.

## Rastreabilidade

**Objetivos:** OBJ-005 → **Requisitos:** FR-062, FR-063 → **Regras:** BR-018 → **História:** US-020 → **Aceitação:** AC-066, AC-067.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-021"></a>
## US-021 — Acompanhar correção e reincidência

**ID:** US-021
**Epic:** EPIC-005 — Retornos e tratamento de ocorrências
**Feature:** FEAT-011 — Advertências e correção
**Objetivo:** Permitir ao Supervisor acompanhar solução do problema.
**Ator:** Supervisor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Dá continuidade ao tratamento de ocorrências não corrigidas.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Supervisor, quero acompanhar a correção do problema, para tratar reincidências conforme a regra de advertência.

## Descrição detalhada

Permitir ao Supervisor acompanhar solução do problema. Problema, situação de correção e advertência anterior. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Problema e advertência registrados; Supervisor autenticado.

## Fluxo principal

1. Consultar problema e advertências anteriores.
2. Acompanhar se houve correção.
3. Quando não corrigido, aplicar o tratamento de reincidência conforme fórmula a definir.

## Fluxos alternativos

Problema corrigido não se enquadra na condição de nova advertência em dobro.

## Exceções

Fórmula da advertência em dobro não definida; não calcular punição por inferência.

## Regras de negócio relacionadas

- **BR-018:** Retorno inadequado gera tratamento de advertências conforme regra definida.

## Requisitos relacionados

- **FR-064:** Permitir ao Supervisor acompanhar a correção do problema.
- **FR-065:** Quando o problema não for corrigido, considerar a nova advertência em dobro em relação à anterior.

## Validações

A condição é problema não corrigido; o cálculo permanece OPEN-002.

## Dados envolvidos

Problema, situação de correção e advertência anterior.

## Dependências

- US-020 — Controlar histórico de advertências

## Critérios de aceitação

- [ ] **AC-068** — Dado um problema registrado, então o Supervisor pode acompanhar sua correção.
- [ ] **AC-069** *(condicionado ao refinamento indicado)* — Dado problema não corrigido, então a regra de negócio exige nova advertência em dobro da anterior; o teste numérico depende da fórmula a definir em OPEN-002.

## Observações e questões abertas

- Não interpretar em dobro como duas advertências, dobro de salário ou dobro de pontos sem decisão.
- **OPEN-002:** “Nova advertência em dobro” não possui fórmula numérica detalhada.
- **OPEN-029:** Completar contagem de advertências e punição salarial.

## Rastreabilidade

**Objetivos:** OBJ-005 → **Requisitos:** FR-064, FR-065 → **Regras:** BR-018 → **História:** US-021 → **Aceitação:** AC-068, AC-069.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-022"></a>
## US-022 — Analisar morte e encerrar o caso

**ID:** US-022
**Epic:** EPIC-005 — Retornos e tratamento de ocorrências
**Feature:** FEAT-012 — Análise de morte
**Objetivo:** Registrar devolução do corpo, análise e resultado da ocorrência.
**Ator:** Gestor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Documenta o caso e separa morte natural do contador normal.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero registrar o resultado da análise de morte realizada pelo Supervisor, para encerrar o caso e distinguir a advertência por morte natural.

## Descrição detalhada

Registrar devolução do corpo, análise e resultado da ocorrência. Humano, devolução do corpo, procedimento, envolvidos, causa e resultado. Causa natural, advertência de cuidado, resultado e encerramento do caso. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Morte durante missão; Supervisor para análise e Gestor para registrar resultado.

## Fluxo principal

1. Registrar devolução do corpo ao local da abdução.
2. Supervisor analisa procedimento, humano, envolvidos e causa.
3. Gestor registra resultado; em causa natural, registra advertência de cuidado separada.
4. Encerrar definitivamente o caso após registrar o resultado.

## Fluxos alternativos

Falha atribuível segue a história de registro de punição.

## Exceções

Resultado ausente impede satisfazer condição de encerramento; estado da missão em análise não foi definido.

## Regras de negócio relacionadas

- **BR-019:** Morte natural gera advertência de cuidado fora do contador normal.
- **BR-020:** Em caso de morte, o resultado da análise deve ser registrado antes do encerramento definitivo do caso.

## Requisitos relacionados

- **FR-066:** Não incluir advertência relacionada a morte natural no contador normal de advertências.
- **FR-067:** Registrar a devolução do corpo ao local da abdução em caso de morte.
- **FR-068:** Permitir ao Supervisor analisar o procedimento, o humano, as pessoas envolvidas e a causa da morte.
- **FR-069:** Permitir ao Gestor registrar o resultado da análise.
- **FR-070:** Registrar advertência específica relacionada ao cuidado quando a causa for natural, sem incluí-la no contador normal.
- **FR-072:** Encerrar definitivamente o caso após o registro do resultado da análise.

## Validações

Morte natural fora do contador normal; resultado precede encerramento.

## Dados envolvidos

Humano, devolução do corpo, procedimento, envolvidos, causa e resultado.

Causa natural, advertência de cuidado, resultado e encerramento do caso.

## Dependências

- US-008 — Iniciar missão e registrar saída
- US-020 — Controlar histórico de advertências

## Critérios de aceitação

- [ ] **AC-070** — Dada morte durante a missão, então o registro contempla devolução do corpo ao local da abdução.
- [ ] **AC-071** — Então o Supervisor pode analisar procedimento, humano, envolvidos e causa da morte.
- [ ] **AC-072** — Dada a análise realizada, então o Gestor pode registrar seu resultado.
- [ ] **AC-073** — Dada análise com causa natural, então a advertência específica de cuidado não integra o contador normal.
- [ ] **AC-074** — Dado resultado da análise registrado, então o caso é encerrado definitivamente.
- [ ] **AC-075** — Dado resultado ainda não registrado, então a pré-condição de encerramento do caso não está satisfeita.

## Observações e questões abertas

- Não criar estado adicional da missão; não incluir ocultação ou falsificação da causa da morte.
- Encerrar o caso não define automaticamente um novo estado nem resolve o estado da missão.
- **OPEN-001:** Não foi definido um estado específico da missão durante a análise de morte. Não criar novo status sem decisão.
- **OPEN-018:** Definir retorno e encerramento em missões com vários humanos.

## Rastreabilidade

**Objetivos:** OBJ-005 → **Requisitos:** FR-066, FR-067, FR-068, FR-069, FR-070, FR-072 → **Regras:** BR-019, BR-020 → **História:** US-022 → **Aceitação:** AC-070, AC-071, AC-072, AC-073, AC-074, AC-075.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-023"></a>
## US-023 — Registrar punição por falha atribuível

**ID:** US-023
**Epic:** EPIC-005 — Retornos e tratamento de ocorrências
**Feature:** FEAT-012 — Análise de morte
**Objetivo:** Manter a responsabilização resultante da análise de morte.
**Ator:** Gestor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Preserva a decisão aplicada aos envolvidos no caso.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor, quero registrar a punição decorrente da análise, para documentar a responsabilização definida no caso.

## Descrição detalhada

Manter a responsabilização resultante da análise de morte. Resultado da análise, envolvidos e punição aplicável. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Análise registrada, falha atribuída e punição previamente determinada por decisão humana.

## Fluxo principal

1. Consultar resultado da análise.
2. Identificar envolvidos e punição aplicável.
3. Gestor registra a punição relacionada ao caso.

## Fluxos alternativos

Causa natural segue advertência de cuidado, não esta condição de falha.

## Exceções

Critérios de julgamento e natureza da punição não definidos.

## Regras de negócio relacionadas

- **BR-020:** Em caso de morte, o resultado da análise deve ser registrado antes do encerramento definitivo do caso.

## Requisitos relacionados

- **FR-071:** Registrar a punição aplicável quando houver falha atribuível aos envolvidos.

## Validações

Registrar a decisão; não automatizar julgamento nem desconto salarial.

## Dados envolvidos

Resultado da análise, envolvidos e punição aplicável.

## Dependências

- US-022 — Analisar morte e encerrar o caso

## Critérios de aceitação

- [ ] **AC-076** — Dada análise que atribua falha aos envolvidos e punição definida, quando o Gestor registrar o resultado, então a punição aplicável é registrada junto ao caso.

## Observações e questões abertas

- Critérios de julgamento e punições não definidos impedem testar a escolha da punição; não presumir cálculo automático.
- **OPEN-013:** O tratamento de punições por falha atribuível em caso de morte não define critérios objetivos de julgamento.
- **OPEN-029:** Completar contagem de advertências e punição salarial.

## Rastreabilidade

**Objetivos:** OBJ-005 → **Requisitos:** FR-071 → **Regras:** BR-020 → **História:** US-023 → **Aceitação:** AC-076.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-024"></a>
## US-024 — Registrar e consultar dados científicos

**ID:** US-024
**Epic:** EPIC-006 — Pesquisa científica
**Feature:** FEAT-013 — Coleta, manutenção e consulta
**Objetivo:** Manter dados científicos com consulta e alteração por perfis autorizados.
**Ator:** Cientista
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Disponibiliza informação científica para necessidades futuras, com restrição de acesso.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Cientista, quero registrar, alterar e consultar dados científicos conforme as permissões de cada perfil, para manter informações úteis para pesquisas futuras.

## Descrição detalhada

Manter dados científicos com consulta e alteração por perfis autorizados. Humano, altura, peso, cor, etnia, DNA e tipo sanguíneo. Dados científicos e perfil do funcionário. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Abdução realizada e humano identificado; usuário autenticado no perfil necessário.

## Fluxo principal

1. Cientista registra altura, peso, cor, etnia, DNA e tipo sanguíneo.
2. Manter dados para consulta por Cientista, Gestor ou Supervisor.
3. Permitir alteração somente a Cientistas.

## Fluxos alternativos

Gestor/Supervisor consulta sem receber permissão de alteração científica.

## Exceções

Demais perfis não consultam dados científicos; não ampliar acesso por histórico.

## Regras de negócio relacionadas

- **BR-021:** Somente Cientistas alteram dados científicos.

## Requisitos relacionados

- **FR-073:** Permitir ao Cientista coletar e registrar dados científicos após a abdução.
- **FR-074:** Manter os dados científicos definidos: altura, peso, cor, etnia, DNA e tipo sanguíneo.
- **FR-075:** Armazenar os dados científicos para necessidades futuras.
- **FR-076:** Permitir consulta dos dados científicos somente por Cientistas, Gestor e Supervisor.
- **FR-077:** Permitir alteração dos dados científicos somente por Cientistas.

## Validações

Distinguir consulta de alteração; formatos/unidades ainda em OPEN-023.

## Dados envolvidos

Humano, altura, peso, cor, etnia, DNA e tipo sanguíneo.

Dados científicos e perfil do funcionário.

## Dependências

- US-001 — Cadastrar e consultar humanos
- US-008 — Iniciar missão e registrar saída

## Critérios de aceitação

- [ ] **AC-077** — Dada abdução realizada, quando o Cientista registrar dados científicos, então os campos previstos em FR-074 podem ser mantidos para consulta futura.
- [ ] **AC-078** — Dado Cientista autenticado, quando alterar dados científicos, então a alteração é permitida.
- [ ] **AC-079** — Dado usuário que não seja Cientista, inclusive Gestor ou Supervisor, quando tentar alterar esses dados, então a alteração é impedida por BR-021.
- [ ] **AC-080** — Dado Cientista, Gestor ou Supervisor autenticado, quando consultar dados científicos existentes, então a consulta é permitida.
- [ ] **AC-081** — Dado Piloto, Abduzidor ou Pesquisador, quando tentar consultar os dados científicos, então a consulta é impedida.

## Observações e questões abertas

- Unidades, formatos e obrigatoriedade dos campos não estão definidos. Não inventar workflow de progresso científico para OPEN-010.
- Evitar ampliar acesso por meio do histórico geral; a delimitação do conteúdo depende de OPEN-016.
- **OPEN-010:** O levantamento não definiu fluxo formal de etapas/status para o progresso da pesquisa científica.
- **OPEN-016:** Delimitar o histórico geral diante dos dados científicos e da auditoria restritos.
- **OPEN-023:** Definir validações dos dados cadastrais e científicos.

## Rastreabilidade

**Objetivos:** OBJ-006 → **Requisitos:** FR-073, FR-074, FR-075, FR-076, FR-077 → **Regras:** BR-021 → **História:** US-024 → **Aceitação:** AC-077, AC-078, AC-079, AC-080, AC-081.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-025"></a>
## US-025 — Tratar obsolescência científica

**ID:** US-025
**Epic:** EPIC-006 — Pesquisa científica
**Feature:** FEAT-014 — Obsolescência científica
**Objetivo:** Excluir dados declarados obsoletos por Gestor/Supervisor.
**Ator:** Gestor ou Supervisor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Evita manter dados científicos considerados sem utilidade.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero determinar a obsolescência dos dados, para retirar informações consideradas obsoletas.

## Descrição detalhada

Excluir dados declarados obsoletos por Gestor/Supervisor. Dados científicos e decisão de obsolescência. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Dados existentes; Gestor/Supervisor autenticado para decisão de obsolescência.

## Fluxo principal

1. Identificar dados científicos obsoletos.
2. Gestor/Supervisor determina a obsolescência.
3. Excluir os dados conforme decisão, sem registro específico da exclusão.

## Fluxos alternativos

Dados ainda não declarados obsoletos permanecem para necessidades futuras.

## Exceções

Prazo de exclusão, granularidade e relação com auditoria estão pendentes.

## Regras de negócio relacionadas

- **BR-022:** Gestor/Supervisor podem determinar obsolescência dos dados científicos.

## Requisitos relacionados

- **FR-078:** Permitir ao Gestor ou Supervisor decidir que dados científicos são obsoletos.
- **FR-079:** Excluir imediatamente os dados científicos considerados obsoletos.
- **FR-080:** Não manter registro específico da exclusão de dados científicos.

## Validações

Permissão administrativa para obsolescência; preservar FR-080 sem inventar trilha específica de exclusão.

## Dados envolvidos

Dados científicos e decisão de obsolescência.

## Dependências

- US-024 — Registrar e consultar dados científicos

## Critérios de aceitação

- [ ] **AC-082** — Dado Gestor ou Supervisor, então pode determinar que dados científicos são obsoletos.
- [ ] **AC-083** *(condicionado ao refinamento indicado)* — Dada a decisão de obsolescência, então os dados são excluídos; o prazo de imediatamente depende de OPEN-006.
- [ ] **AC-084** — Então não se mantém registro específico dessa exclusão, conforme FR-080; a relação com a auditoria exige delimitação em OPEN-003.

## Observações e questões abertas

- Granularidade da exclusão e relação com valores preservados na auditoria não estão definidas.
- **OPEN-003:** Auditoria de exclusão de dados científicos não foi detalhada; permanece a decisão explícita de não manter registro específico da exclusão.
- **OPEN-006:** FR-079 usa “imediatamente” para exclusão de dados obsoletos, sem limite temporal verificável.
- **OPEN-030:** Delimitar exclusão científica e dados preservados em auditoria.

## Rastreabilidade

**Objetivos:** OBJ-006 → **Requisitos:** FR-078, FR-079, FR-080 → **Regras:** BR-022 → **História:** US-025 → **Aceitação:** AC-082, AC-083, AC-084.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-026"></a>
## US-026 — Consultar histórico das missões

**ID:** US-026
**Epic:** EPIC-007 — Histórico e auditoria
**Feature:** FEAT-015 — Consulta e correção do histórico
**Objetivo:** Permitir aos funcionários acompanhar missões e ocorrências.
**Ator:** funcionário
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Centraliza o registro operacional e dispensa relatório separado.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como funcionário, quero consultar o histórico das missões, para acompanhar operações e ocorrências.

## Descrição detalhada

Permitir aos funcionários acompanhar missões e ocorrências. Histórico de missões e ocorrências. Pré-condição: funcionário autenticado. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Funcionário autenticado; missões/histórico existentes.

## Fluxo principal

1. Solicitar consulta ao histórico.
2. Exibir registros de missões e ocorrências previstos.
3. Permitir leitura conforme permissão geral dos funcionários.

## Fluxos alternativos

Todos os perfis de funcionários podem consultar; humano não é usuário.

## Exceções

Delimitar histórico diante de dados científicos/auditoria restritos em OPEN-016.

## Regras de negócio relacionadas

- **BR-023:** Todos os funcionários consultam o histórico; alteração é restrita a Gestor/Supervisor.

## Requisitos relacionados

- **FR-081:** Manter o histórico das missões como registro suficiente, sem relatório separado de missão.
- **FR-082:** Permitir consulta do histórico completo a todos os funcionários.

## Validações

Autenticação; consulta a todos os funcionários; não exigir relatório separado.

## Dados envolvidos

Histórico de missões e ocorrências. Pré-condição: funcionário autenticado.

## Dependências

- US-006 — Definir missão, tripulação e capacidade

## Critérios de aceitação

- [ ] **AC-085** — Dado qualquer perfil de funcionário autenticado, quando consultar o histórico, então a consulta é permitida.
- [ ] **AC-086** — Então o histórico contém os registros de missões e ocorrências previstas no Discovery.
- [ ] **AC-087** — Então o histórico satisfaz o registro da missão sem exigir relatório separado.

## Observações e questões abertas

- Histórico completo deve ser delimitado perante dados científicos restritos e auditoria administrativa.
- **OPEN-016:** Delimitar o histórico geral diante dos dados científicos e da auditoria restritos.

## Rastreabilidade

**Objetivos:** OBJ-005, OBJ-007 → **Requisitos:** FR-081, FR-082 → **Regras:** BR-023 → **História:** US-026 → **Aceitação:** AC-085, AC-086, AC-087.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-027"></a>
## US-027 — Corrigir histórico com permissão administrativa

**ID:** US-027
**Epic:** EPIC-007 — Histórico e auditoria
**Feature:** FEAT-015 — Consulta e correção do histórico
**Objetivo:** Permitir manutenção do histórico pelos administradores.
**Ator:** Gestor ou Supervisor
**Prioridade:** Média — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Possibilita corrigir registros operacionais sob responsabilidade definida.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero alterar o histórico das missões, para corrigir seus registros conforme minha permissão.

## Descrição detalhada

Permitir manutenção do histórico pelos administradores. Histórico e dados alterados. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Histórico existente; Gestor/Supervisor autenticado.

## Fluxo principal

1. Selecionar o registro histórico.
2. Gestor/Supervisor altera o conteúdo autorizado.
3. Manter a alteração no histórico da missão.

## Fluxos alternativos

Outros funcionários continuam com consulta, sem alteração.

## Exceções

Histórico editável não concede edição da trilha de auditoria.

## Regras de negócio relacionadas

- **BR-023:** Todos os funcionários consultam o histórico; alteração é restrita a Gestor/Supervisor.

## Requisitos relacionados

- **FR-083:** Permitir alteração do histórico somente ao Gestor e Supervisor.

## Validações

Restringir alteração a Gestor/Supervisor; eventos auditáveis em OPEN-032.

## Dados envolvidos

Histórico e dados alterados.

## Dependências

- US-026 — Consultar histórico das missões

## Critérios de aceitação

- [ ] **AC-088** — Dado Gestor ou Supervisor, quando alterar o histórico, então a alteração é permitida.
- [ ] **AC-089** — Dado outro perfil de funcionário, quando tentar alterar o histórico, então a alteração é impedida.
- [ ] **AC-090** — Então alteração de histórico não concede permissão para alterar registros imutáveis de auditoria (US-030).

## Observações e questões abertas

- Eventos de alteração do histórico abrangidos pela auditoria devem constar no catálogo de alterações relevantes.
- **OPEN-032:** Definir quais alterações são relevantes para auditoria.

## Rastreabilidade

**Objetivos:** OBJ-005, OBJ-007 → **Requisitos:** FR-083 → **Regras:** BR-023 → **História:** US-027 → **Aceitação:** AC-088, AC-089, AC-090.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-028"></a>
## US-028 — Registrar tentativas de acesso

**ID:** US-028
**Epic:** EPIC-007 — Histórico e auditoria
**Feature:** FEAT-016 — Trilhas de acesso, alteração e consulta
**Objetivo:** Manter registros de autenticação por dois meses.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Permite examinar acessos bem-sucedidos e malsucedidos.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero dispor dos registros de tentativas de acesso, para acompanhar a autenticação no período definido.

## Descrição detalhada

Manter registros de autenticação por dois meses. Usuário, data/hora e resultado da tentativa. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Tentativa de autenticação realizada.

## Fluxo principal

1. Capturar identificação disponível, data/hora e resultado.
2. Registrar tanto tentativas aceitas quanto negadas.
3. Reter os registros pelo período de dois meses definido.

## Fluxos alternativos

Tentativa malsucedida também é registrada.

## Exceções

Login inexistente, cálculo de meses e tratamento após retenção em OPEN-031.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-014:** Registrar tentativas de acesso bem-sucedidas e malsucedidas.
- **FR-085:** Reter auditoria de acessos por 2 meses.

## Validações

Não omitir falhas; manter resultado e referência temporal.

## Dados envolvidos

Usuário, data/hora e resultado da tentativa.

## Dependências

- US-015 — Autenticar funcionário por login e senha

## Critérios de aceitação

- [ ] **AC-091** — Dada tentativa bem-sucedida, então se registra usuário, data/hora e resultado.
- [ ] **AC-092** — Dada tentativa malsucedida, então também se registra o resultado e os dados de identificação disponíveis.
- [ ] **AC-093** *(condicionado ao refinamento indicado)* — Então os registros de acesso têm retenção de 2 meses; cálculo do prazo e tratamento após seu término dependem de OPEN-031.

## Observações e questões abertas

- Acesso administrativo a esses registros e login inexistente precisam de detalhamento; não inventar retenção permanente.
- **OPEN-031:** Detalhar retenção e expiração de auditoria.

## Rastreabilidade

**Objetivos:** OBJ-005, OBJ-007 → **Requisitos:** FR-014, FR-085 → **Regras:** condições dos FR → **História:** US-028 → **Aceitação:** AC-091, AC-092, AC-093.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-029"></a>
## US-029 — Auditar alterações relevantes

**ID:** US-029
**Epic:** EPIC-007 — Histórico e auditoria
**Feature:** FEAT-016 — Trilhas de acesso, alteração e consulta
**Objetivo:** Registrar autoria e valores de alterações por seis meses.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Permite rastrear mudanças de funcionários, naves, missões e dados científicos.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero dispor de trilha das alterações relevantes, para identificar autoria e mudanças nos dados.

## Descrição detalhada

Registrar autoria e valores de alterações por seis meses. Usuário, data/hora, registro/dado, valor anterior e novo valor. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Alteração classificada como relevante em um domínio coberto.

## Fluxo principal

1. Identificar usuário e dado/registro alterado.
2. Registrar data/hora, valor anterior e novo valor.
3. Reter a trilha de alteração por seis meses.

## Fluxos alternativos

Eventos fora do catálogo relevante não têm tratamento definido.

## Exceções

Catálogo, valores sensíveis e conflito com exclusão científica permanecem pendentes.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-015:** Registrar alterações relevantes de dados de funcionários, naves, missões e dados científicos.
- **FR-086:** Reter auditoria de alterações por 6 meses.
- **FR-087:** Registrar em auditoria de alteração: usuário, data/hora, registro/dado alterado, valor anterior e novo valor.

## Validações

Campos de FR-087; retenção declarada; não inferir armazenamento de senha em texto.

## Dados envolvidos

Usuário, data/hora, registro/dado, valor anterior e novo valor.

## Dependências

- US-004 — Manter cadastro e manutenção das naves
- US-006 — Definir missão, tripulação e capacidade
- US-013 — Administrar cadastro de funcionários
- US-024 — Registrar e consultar dados científicos

## Critérios de aceitação

- [ ] **AC-094** *(condicionado ao refinamento indicado)* — Dada alteração classificada como relevante em funcionário, nave, missão ou dados científicos, então a auditoria registra usuário, data/hora, registro/dado, valor anterior e novo valor.
- [ ] **AC-095** — Então os registros de alteração têm retenção de 6 meses.

## Observações e questões abertas

- Catálogo de eventos, tratamento de credenciais e dados sensíveis e convivência com exclusão científica dependem de refinamento.
- **OPEN-003:** Auditoria de exclusão de dados científicos não foi detalhada; permanece a decisão explícita de não manter registro específico da exclusão.
- **OPEN-030:** Delimitar exclusão científica e dados preservados em auditoria.
- **OPEN-031:** Detalhar retenção e expiração de auditoria.
- **OPEN-032:** Definir quais alterações são relevantes para auditoria.

## Rastreabilidade

**Objetivos:** OBJ-005, OBJ-007 → **Requisitos:** FR-015, FR-086, FR-087 → **Regras:** condições dos FR → **História:** US-029 → **Aceitação:** AC-094, AC-095.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

<a id="us-030"></a>
## US-030 — Consultar e proteger a auditoria

**ID:** US-030
**Epic:** EPIC-007 — Histórico e auditoria
**Feature:** FEAT-016 — Trilhas de acesso, alteração e consulta
**Objetivo:** Restringir consulta e impedir edição das evidências de alteração.
**Ator:** Gestor ou Supervisor
**Prioridade:** Alta — proposta para o planejamento acadêmico; não é uma decisão atribuída ao stakeholder.
**Valor de negócio:** Mantém rastreabilidade da fiscalização administrativa.
**Status do Discovery:** Refining — requer os esclarecimentos indicados em OPEN.

## História de usuário

Como Gestor ou Supervisor, quero consultar a auditoria com rastreamento, para fiscalizar alterações sem modificar suas evidências.

## Descrição detalhada

Restringir consulta e impedir edição das evidências de alteração. Registro de auditoria, usuário consultante, data/hora e registro consultado. A operação se limita às regras e aos requisitos relacionados abaixo.

## Pré-condições

Registro de alteração existente; Gestor/Supervisor autenticado para consulta.

## Fluxo principal

1. Gestor/Supervisor consulta um registro de auditoria.
2. Sistema registra consultante, data/hora e registro consultado.
3. Manter a trilha de alterações somente para leitura.

## Fluxos alternativos

Usuário de outro perfil não pode consultar a auditoria de alterações.

## Exceções

Nenhum perfil pode alterar/excluir manualmente registros; expiração por prazo depende de OPEN-031.

## Regras de negócio relacionadas

Condições descritas nos requisitos funcionais de origem; não há BR específica adicional identificada.

## Requisitos relacionados

- **FR-016:** Permitir consulta dos registros de alteração somente ao Gestor e Supervisor.
- **FR-017:** Manter registros de alteração somente para leitura, sem permitir sua alteração ou exclusão.
- **FR-018:** Registrar quem consultou registros de auditoria, data/hora e qual registro foi consultado.
- **FR-088:** Registrar em auditoria de consulta de auditoria: usuário, data/hora e registro de auditoria consultado.

## Validações

Permissão administrativa; imutabilidade; registro de cada consulta.

## Dados envolvidos

Registro de auditoria, usuário consultante, data/hora e registro consultado.

## Dependências

- US-029 — Auditar alterações relevantes

## Critérios de aceitação

- [ ] **AC-096** — Dado Gestor ou Supervisor, quando consultar registros de alteração, então a consulta é permitida; para os demais perfis é impedida.
- [ ] **AC-097** — Dado qualquer perfil, quando tentar editar ou excluir um registro de alteração, então a operação não é permitida.
- [ ] **AC-098** — Dada consulta de auditoria, então se registra quem consultou, data/hora e qual registro foi consultado.

## Observações e questões abertas

- FR-018 e FR-088 são tratados em uma história. Retenção do registro de consulta e expiração administrada versus exclusão por usuário precisam ser esclarecidas.
- **OPEN-031:** Detalhar retenção e expiração de auditoria.

## Rastreabilidade

**Objetivos:** OBJ-005, OBJ-007 → **Requisitos:** FR-016, FR-017, FR-018, FR-088 → **Regras:** condições dos FR → **História:** US-030 → **Aceitação:** AC-096, AC-097, AC-098.

**Base:** adaptação do Discovery SGA de referência fornecido por Richard para esta organização. A ordem e o agrupamento das histórias são próprios deste backlog. Prioridades são propostas; questões abertas não representam respostas confirmadas de Pedro.

