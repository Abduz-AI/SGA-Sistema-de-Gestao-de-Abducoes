# SGA — Discovery consolidado

**Organização:** Abduz-AI | **Versão:** 1.0 | **Data:** 01/10/2026
**Situação:** baseline acadêmica adaptada, com questões abertas identificadas. Escopo exclusivo de Discovery; sem arquitetura ou implementação.

## 1. Contexto e fontes

O Sistema de Gestão de Abduções (SGA) centraliza funcionários, naves, humanos, pesquisas e missões da organização fictícia Abduz.AI. O processo de referência utilizava AlienZap e apresentava conflitos de agendamento, uso de naves em manutenção e dispersão dos registros operacionais.

Esta versão foi preparada para o repositório `Abduz-AI/SGA-Sistema-de-Gestao-de-Abducoes`, identificado na organização de Pedro Roman. Por solicitação de Richard, utiliza como referência o Discovery já consolidado do mesmo exercício. Não representa uma nova entrevista realizada com Pedro.

Fontes utilizadas:
- Especificação formal de requisitos SGA v1.1 e documento consolidado v1.0 fornecidos na conversa e refletidos no repositório de referência.
- [Backlog e rastreabilidade do SGA de referência](https://github.com/Projeto-Abduz-AI/Projeto_Abduz.AI-SGA/tree/main/docs/discovery/backlog), consultados para esta adaptação.
- Decisões do Discovery registradas no contexto fornecido por Richard.
- Prompt integral do professor “Chat 03 — Backlog”, fornecido em 30/09/2026.

Os requisitos FR, BR, NFR, OBJ, DEC e OPEN preservam os identificadores da referência. EPIC, FEAT, US e AC pertencem a esta versão de Abduz-AI e não devem ser confundidos com os IDs de histórias do outro grupo. Prioridades são propostas editoriais. Nenhuma resposta foi atribuída a Pedro sem registro.

## 2. Objetivos

| ID | Objetivo |
|---|---|
| OBJ-001 | Centralizar o controle das abduções, naves, funcionários, humanos e missões. |
| OBJ-002 | Reduzir conflitos de agendamento de missões. |
| OBJ-003 | Impedir o uso de naves indisponíveis ou em manutenção. |
| OBJ-004 | Impedir conflitos de participação de funcionários e de humanos em missões. |
| OBJ-005 | Manter o histórico das missões e das ocorrências fora do padrão. |
| OBJ-006 | Controlar informações e dados científicos relacionados aos humanos. |
| OBJ-007 | Controlar o acesso ao sistema e registrar atividades relevantes de usuários. |

## 3. Stakeholders e atores

| Stakeholder | Ator | Papel |
|---|---|
| STK-001 — Organização Abduz.AI | — | Solicita e utiliza o SGA para centralizar a operação. |
| STK-002 — Gestor | ACT-001 | Define missões, administra cadastros e registra resultados/ocorrências. |
| STK-003 — Supervisor | ACT-002 | Administra o sistema, avalia pesquisas e analisa ocorrências. |
| STK-004 — Piloto | ACT-003 | Participa da tripulação e do deslocamento da nave. |
| STK-005 — Abduzidor | ACT-004 | Participa da abdução e do retorno dos humanos. |
| STK-006 — Pesquisador | ACT-005 | Registra pesquisa pré-missão sobre humanos e locais. |
| STK-007 — Cientista | ACT-006 | Registra, consulta e altera dados científicos. |
| Funcionários, categoria que reúne os perfis internos | ACT-007 | Autenticam-se e consultam histórico conforme permissões. |
| STK-008 — Humano envolvido | ACT-008, participante do domínio | Alvo/participante da missão; não é usuário do SGA. |

## 4. Escopo e restrições

**Incluído:** cadastros; autenticação; manutenção e autonomia de naves; pesquisa pré-missão; planejamento, agendamento e ciclo das missões; notificações; retornos e advertências; análise de morte; dados científicos; histórico; auditoria.

**Fora do escopo consolidado:** integração com Área 51; relatório separado de missão; ocultação/falsificação da causa de morte; rastreamento da posição atual da nave; integração automática com folha salarial. Não foram acrescentados mapas, aplicativo móvel, IA classificadora ou controles de combustível.

**Restrições:** acesso às missões exige autenticação; permissões seguem os perfis; status de missão permanecem os cinco definidos; cancelamento definitivo não é remarcação; decisões de tecnologia, infraestrutura e banco ficam para fases futuras.

## 5. Fluxo geral do negócio

1. Cadastrar humanos, funcionários e naves.
2. Pesquisador registra informações de vida e localização para a pesquisa pré-missão.
3. Gestor/Supervisor avalia a pesquisa; relevância global impede prosseguimento e gera cancelamento definitivo.
4. Sem impedimento relevante, Gestor decide prosseguir e define humanos, nave, tripulação, local, data e horário.
5. SGA verifica disponibilidade, sobreposição, tripulação mínima, capacidade e autonomia de ida e volta.
6. Agendamento válido permanece Pendente; no horário marcado, passa automaticamente para Em andamento e registra saída da nave.
7. Registrar retorno normal ou ocorrência fora do padrão; coletar dados científicos após a abdução conforme os perfis.
8. No encerramento normal, Gestor informa término; a missão passa a Concluída e a entrada da nave é registrada.
9. Ocorrências de morte são analisadas pelo Supervisor e têm resultado registrado pelo Gestor antes do encerramento definitivo do caso.
10. Histórico e auditoria seguem permissões e retenções consolidadas.

## 6. Estados da missão

| Estado/evento | Comportamento definido |
|---|---|
| Pendente | Missão agendada com validações satisfeitas. |
| Pendente → Em andamento | Mudança automática no horário agendado; saída da nave registrada. |
| Em andamento → Concluída | No encerramento normal, Gestor informa término; entrada registrada. |
| Adiada | Aguarda nova data; estados de origem permitidos ainda dependem de OPEN-028. |
| Adiada → Pendente | Gestor/Supervisor informa nova data; preserva o registro. |
| Cancelada | Estado definitivo; registrar responsável e motivo. |
| Concluída | Estado definitivo. |
| Análise de morte | Nenhum status adicional autorizado; OPEN-001. |

Os estados do Kanban são estados do trabalho da equipe e não devem ser confundidos com estados das missões do SGA.

## 7. Requisitos funcionais

Os requisitos abaixo mantêm o texto consolidado de origem. Os fluxos, exceções, validações e critérios de teste derivados estão nas [30 histórias](BACKLOG.md). Termos ainda imprecisos são explicitados como OPEN.

| ID | Requisito | História desta versão |
|---|---|---|
| FR-001 | Permitir o cadastro e alteração de funcionários pelo Gestor ou Supervisor. | [US-013](BACKLOG.md#us-013) |
| FR-002 | Manter funcionário desligado/inativo sem excluí-lo do sistema. | [US-014](BACKLOG.md#us-014) |
| FR-003 | Impedir a seleção de funcionário inativo para novas missões. | [US-014](BACKLOG.md#us-014) |
| FR-004 | Permitir a reativação de funcionário inativo pelo Gestor ou Supervisor, sem condição ou justificativa adicional. | [US-014](BACKLOG.md#us-014) |
| FR-005 | Permitir autenticação por login/usuário e senha. | [US-015](BACKLOG.md#us-015) |
| FR-006 | Garantir que o login seja único no SGA. | [US-013](BACKLOG.md#us-013) |
| FR-007 | Bloquear temporariamente a conta após 5 tentativas consecutivas de senha incorreta. | [US-016](BACKLOG.md#us-016) |
| FR-008 | Manter o bloqueio por 15 minutos ou até aprovação do Gestor/Supervisor, o que ocorrer primeiro. | [US-016](BACKLOG.md#us-016) |
| FR-009 | Alertar imediatamente Gestor e Supervisor sobre o bloqueio por tentativas incorretas, dentro do SGA e por e-mail, indicando caráter crítico/possível risco de intrusão. | [US-016](BACKLOG.md#us-016) |
| FR-010 | Permitir alteração de senha somente mediante solicitação do funcionário e aprovação do Gestor ou Supervisor. | [US-017](BACKLOG.md#us-017) |
| FR-011 | Aplicar o mesmo procedimento de aprovação para esquecimento de senha. | [US-017](BACKLOG.md#us-017) |
| FR-012 | Bloquear imediatamente o acesso de funcionário inativo/desligado. | [US-014](BACKLOG.md#us-014) |
| FR-013 | Encerrar automaticamente a sessão ao final do dia de trabalho; as credenciais são exigidas novamente no próximo acesso. | [US-018](BACKLOG.md#us-018) |
| FR-014 | Registrar tentativas de acesso bem-sucedidas e malsucedidas. | [US-028](BACKLOG.md#us-028) |
| FR-015 | Registrar alterações relevantes de dados de funcionários, naves, missões e dados científicos. | [US-029](BACKLOG.md#us-029) |
| FR-016 | Permitir consulta dos registros de alteração somente ao Gestor e Supervisor. | [US-030](BACKLOG.md#us-030) |
| FR-017 | Manter registros de alteração somente para leitura, sem permitir sua alteração ou exclusão. | [US-030](BACKLOG.md#us-030) |
| FR-018 | Registrar quem consultou registros de auditoria, data/hora e qual registro foi consultado. | [US-030](BACKLOG.md#us-030) |
| FR-019 | Permitir cadastrar e alterar dados de naves. | [US-004](BACKLOG.md#us-004) |
| FR-020 | Manter para a nave os dados definidos: capacidade total, quilômetros que pode voar e status operacional. | [US-004](BACKLOG.md#us-004) |
| FR-021 | Permitir alterar o status operacional entre disponível e manutenção pelo Gestor ou Supervisor. | [US-004](BACKLOG.md#us-004) |
| FR-022 | Impedir a utilização de nave em manutenção em uma missão. | [US-004](BACKLOG.md#us-004) |
| FR-023 | Registrar automaticamente a saída da nave quando a missão entrar em Em andamento. | [US-008](BACKLOG.md#us-008) |
| FR-024 | Registrar automaticamente a entrada da nave quando a missão passar para Concluída. | [US-009](BACKLOG.md#us-009) |
| FR-025 | Considerar o Estacionamento Alien como ponto de partida das naves. | [US-005](BACKLOG.md#us-005) |
| FR-026 | Considerar o Estacionamento Alien como destino de retorno das naves. | [US-005](BACKLOG.md#us-005) |
| FR-027 | Verificar a autonomia da nave para o percurso completo da missão, incluindo ida e retorno. | [US-005](BACKLOG.md#us-005) |
| FR-028 | Permitir cadastrar e consultar humanos. | [US-001](BACKLOG.md#us-001) |
| FR-029 | Manter no cadastro do humano nome, localização, idade e popularidade. | [US-001](BACKLOG.md#us-001) |
| FR-030 | Impedir que um mesmo humano participe de mais de uma missão simultaneamente. | [US-007](BACKLOG.md#us-007) |
| FR-031 | Exigir pesquisa pré-missão antes do agendamento de toda missão. | [US-002](BACKLOG.md#us-002) |
| FR-032 | Permitir ao Pesquisador registrar pesquisa sobre idade, patrimônio/riqueza, emprego, fonte de renda, popularidade, interações sociais e informações gerais da vida. | [US-002](BACKLOG.md#us-002) |
| FR-033 | Permitir ao Pesquisador registrar pesquisa de localização para identificar locais mais calmos. | [US-002](BACKLOG.md#us-002) |
| FR-034 | Permitir que Gestor e Supervisor avaliem as informações da pesquisa. | [US-003](BACKLOG.md#us-003) |
| FR-035 | Não realizar automaticamente a classificação de exceções; a identificação cabe à avaliação humana de Gestor/Supervisor. | [US-003](BACKLOG.md#us-003) |
| FR-036 | Impedir a prossecução da missão quando for identificada relevância em escala global, resultando em cancelamento definitivo. | [US-003](BACKLOG.md#us-003) |
| FR-037 | Quando não houver exceção relevante para impedir a missão, permitir que o Gestor decida se a abdução prosseguirá. | [US-003](BACKLOG.md#us-003) |
| FR-038 | Permitir ao Gestor definir humano, nave, tripulação, local, data e horário da missão. | [US-006](BACKLOG.md#us-006) |
| FR-039 | Permitir ao Gestor iniciar/registrar a solicitação da missão. | [US-006](BACKLOG.md#us-006) |
| FR-040 | Verificar disponibilidade de nave e funcionários antes do agendamento. | [US-007](BACKLOG.md#us-007) |
| FR-041 | Bloquear o agendamento quando houver conflito ou indisponibilidade. | [US-007](BACKLOG.md#us-007) |
| FR-042 | Impedir que funcionário participe de duas missões com horários sobrepostos. | [US-007](BACKLOG.md#us-007) |
| FR-043 | Exigir pelo menos um Piloto e um Abduzidor na tripulação. | [US-006](BACKLOG.md#us-006) |
| FR-044 | Considerar apenas funcionários ativos e disponíveis na seleção da tripulação. | [US-006](BACKLOG.md#us-006) |
| FR-045 | Considerar tripulação e humanos no cálculo da capacidade da nave. | [US-006](BACKLOG.md#us-006) |
| FR-046 | Permitir mais de um humano na mesma missão, desde que respeitada a capacidade da nave. | [US-006](BACKLOG.md#us-006) |
| FR-047 | Bloquear agendamento quando a capacidade da nave for excedida. | [US-006](BACKLOG.md#us-006) |
| FR-048 | Manter os estados de missão: Pendente, Em andamento, Adiada, Concluída e Cancelada. | [US-008](BACKLOG.md#us-008) |
| FR-049 | Alterar automaticamente Pendente para Em andamento no horário agendado. | [US-008](BACKLOG.md#us-008) |
| FR-050 | Permitir ao Gestor informar o término da missão, levando-a para Concluída. | [US-009](BACKLOG.md#us-009) |
| FR-051 | Permitir postergar uma missão. | [US-010](BACKLOG.md#us-010) |
| FR-052 | Manter missão Adiada até que Gestor ou Supervisor defina nova data. | [US-010](BACKLOG.md#us-010) |
| FR-053 | Retornar a missão Adiada para Pendente quando nova data for definida. | [US-010](BACKLOG.md#us-010) |
| FR-054 | Permitir cancelamento por indisponibilidade ou exceção. | [US-011](BACKLOG.md#us-011) |
| FR-055 | Registrar quem cancelou e o motivo do cancelamento. | [US-011](BACKLOG.md#us-011) |
| FR-056 | Considerar cancelamento definitivo, sem reativação ou reagendamento. | [US-011](BACKLOG.md#us-011) |
| FR-057 | Não criar um status chamado Reagendada; uma nova data de missão postergada mantém o mesmo registro e retorna a Pendente. | [US-010](BACKLOG.md#us-010) |
| FR-058 | Enviar notificações internas aos funcionários envolvidos quando houver mudanças relevantes da missão. | [US-012](BACKLOG.md#us-012) |
| FR-059 | Registrar retorno normal como 'retornado com vida'. | [US-019](BACKLOG.md#us-019) |
| FR-060 | Registrar retorno inadequado quando o humano não for devolvido ao local da abdução ou sofrer consequência de saúde no retorno. | [US-019](BACKLOG.md#us-019) |
| FR-061 | Registrar ocorrências fora do padrão no histórico da missão por meio de relato narrativo do Gestor. | [US-019](BACKLOG.md#us-019) |
| FR-062 | Manter histórico de advertências por funcionário. | [US-020](BACKLOG.md#us-020) |
| FR-063 | Aplicar três advertências para retorno inadequado e punição salarial na quarta advertência. | [US-020](BACKLOG.md#us-020) |
| FR-064 | Permitir ao Supervisor acompanhar a correção do problema. | [US-021](BACKLOG.md#us-021) |
| FR-065 | Quando o problema não for corrigido, considerar a nova advertência em dobro em relação à anterior. | [US-021](BACKLOG.md#us-021) |
| FR-066 | Não incluir advertência relacionada a morte natural no contador normal de advertências. | [US-022](BACKLOG.md#us-022) |
| FR-067 | Registrar a devolução do corpo ao local da abdução em caso de morte. | [US-022](BACKLOG.md#us-022) |
| FR-068 | Permitir ao Supervisor analisar o procedimento, o humano, as pessoas envolvidas e a causa da morte. | [US-022](BACKLOG.md#us-022) |
| FR-069 | Permitir ao Gestor registrar o resultado da análise. | [US-022](BACKLOG.md#us-022) |
| FR-070 | Registrar advertência específica relacionada ao cuidado quando a causa for natural, sem incluí-la no contador normal. | [US-022](BACKLOG.md#us-022) |
| FR-071 | Registrar a punição aplicável quando houver falha atribuível aos envolvidos. | [US-023](BACKLOG.md#us-023) |
| FR-072 | Encerrar definitivamente o caso após o registro do resultado da análise. | [US-022](BACKLOG.md#us-022) |
| FR-073 | Permitir ao Cientista coletar e registrar dados científicos após a abdução. | [US-024](BACKLOG.md#us-024) |
| FR-074 | Manter os dados científicos definidos: altura, peso, cor, etnia, DNA e tipo sanguíneo. | [US-024](BACKLOG.md#us-024) |
| FR-075 | Armazenar os dados científicos para necessidades futuras. | [US-024](BACKLOG.md#us-024) |
| FR-076 | Permitir consulta dos dados científicos somente por Cientistas, Gestor e Supervisor. | [US-024](BACKLOG.md#us-024) |
| FR-077 | Permitir alteração dos dados científicos somente por Cientistas. | [US-024](BACKLOG.md#us-024) |
| FR-078 | Permitir ao Gestor ou Supervisor decidir que dados científicos são obsoletos. | [US-025](BACKLOG.md#us-025) |
| FR-079 | Excluir imediatamente os dados científicos considerados obsoletos. | [US-025](BACKLOG.md#us-025) |
| FR-080 | Não manter registro específico da exclusão de dados científicos. | [US-025](BACKLOG.md#us-025) |
| FR-081 | Manter o histórico das missões como registro suficiente, sem relatório separado de missão. | [US-026](BACKLOG.md#us-026) |
| FR-082 | Permitir consulta do histórico completo a todos os funcionários. | [US-026](BACKLOG.md#us-026) |
| FR-083 | Permitir alteração do histórico somente ao Gestor e Supervisor. | [US-027](BACKLOG.md#us-027) |
| FR-084 | Registrar no histórico as ocorrências fora do padrão. | [US-019](BACKLOG.md#us-019) |
| FR-085 | Reter auditoria de acessos por 2 meses. | [US-028](BACKLOG.md#us-028) |
| FR-086 | Reter auditoria de alterações por 6 meses. | [US-029](BACKLOG.md#us-029) |
| FR-087 | Registrar em auditoria de alteração: usuário, data/hora, registro/dado alterado, valor anterior e novo valor. | [US-029](BACKLOG.md#us-029) |
| FR-088 | Registrar em auditoria de consulta de auditoria: usuário, data/hora e registro de auditoria consultado. | [US-030](BACKLOG.md#us-030) |

## 8. Requisitos não funcionais

| ID | Requisito | Critério verificável / situação |
|---|---|---|
| NFR-001 | Disponibilidade 24×7. | Cobrir todos os dias e horários; percentual, janela de medição e manutenção ainda em OPEN-033. |
| NFR-002 | Autenticar acesso às informações de missão. | Tentativa sem autenticação não permite consultar missão; credenciais válidas de conta habilitada permitem entrada. |
| NFR-003 | Prevenir perda e alteração indevida. | Metas de perda/recuperação não definidas, OPEN-004. Não declarar satisfeito apenas por haver auditoria. |
| NFR-004 | Respeitar permissões. | Executar operações com perfil autorizado e não autorizado, verificando concessão/negação. OPEN-016/017 delimitam ambiguidades. |
| NFR-005 | Auditar acessos e alterações relevantes. | Registrar dados definidos; retenção de acessos de 2 meses e alterações de 6 meses. Detalhes de expiração em OPEN-031. |

Não foram inventados tempo de resposta, número de usuários simultâneos, percentual de disponibilidade ou fórmula de recuperação. O refinamento desses pontos permanece proporcional ao escopo acadêmico.

## 9. Regras de negócio

| ID | Regra |
|---|---|
| BR-001 | Gestor e Supervisor possuem poderes iguais no sistema. |
| BR-002 | Funcionário inativo não pode ser selecionado para nova missão. |
| BR-003 | Funcionário inativo não é excluído do sistema e pode ser reativado pelo Gestor ou Supervisor. |
| BR-004 | Nave em manutenção não pode participar de missão. |
| BR-005 | Capacidade da nave inclui tripulação e humanos. |
| BR-006 | Uma missão exige pelo menos um Piloto e um Abduzidor. |
| BR-007 | Um funcionário não pode participar de missões com sobreposição de horários. |
| BR-008 | Um humano não pode participar de mais de uma missão simultaneamente. |
| BR-009 | Pesquisa pré-missão é obrigatória antes do agendamento. |
| BR-010 | A avaliação de exceções é humana, realizada por Gestor e Supervisor. |
| BR-011 | Relevância global impede a prossecução da missão e resulta em cancelamento definitivo. |
| BR-012 | Os estados de missão são Pendente, Em andamento, Adiada, Concluída e Cancelada. |
| BR-013 | Concluída e Cancelada são estados definitivos. |
| BR-014 | Missão Adiada retorna a Pendente quando recebe nova data. |
| BR-015 | Cancelamento exige motivo: indisponibilidade ou exceção. |
| BR-016 | Nave parte e retorna ao Estacionamento Alien. |
| BR-017 | Autonomia considera o percurso completo de ida e retorno. |
| BR-018 | Retorno inadequado gera tratamento de advertências conforme regra definida. |
| BR-019 | Morte natural gera advertência de cuidado fora do contador normal. |
| BR-020 | Em caso de morte, o resultado da análise deve ser registrado antes do encerramento definitivo do caso. |
| BR-021 | Somente Cientistas alteram dados científicos. |
| BR-022 | Gestor/Supervisor podem determinar obsolescência dos dados científicos. |
| BR-023 | Todos os funcionários consultam o histórico; alteração é restrita a Gestor/Supervisor. |

## 10. Dados relevantes

| Grupo | Dados definidos |
|---|---|
| Funcionário | Nome, matrícula/registro, função, cargo, situação, credenciais e histórico de advertências. |
| Nave | Capacidade total, quilômetros disponíveis, status operacional, saída e entrada. |
| Humano | Nome, localização, idade e popularidade. |
| Pesquisa pré-missão | Idade, patrimônio/riqueza, emprego, fonte de renda, popularidade, interações sociais, informações gerais e localização. |
| Missão | Humano(s), nave, tripulação, local, data/horário, estado, término, responsável e motivo de cancelamento, ocorrências. Término previsto versus real em OPEN-007. |
| Retorno e morte | Humano, locais de abdução/devolução, condição de retorno, relato, causa, envolvidos, análise, resultado e punição aplicável. |
| Dados científicos | Altura, peso, cor, etnia, DNA e tipo sanguíneo. |
| Acesso auditado | Usuário/identificação disponível, data/hora e resultado. |
| Alteração auditada | Usuário, data/hora, registro/dado, valor anterior e novo. |
| Consulta de auditoria | Usuário consultante, data/hora e registro consultado. |

## 11. Permissões

| Operação | Permissão consolidada |
|---|---|
| Funcionários, credenciais iniciais, inativação/reativação | Gestor e Supervisor. |
| Login | Funcionário habilitado, sem bloqueio temporário. |
| Troca/recuperação de senha | Solicitação e aprovação de Gestor/Supervisor; executor/canal em OPEN-022. |
| Cadastro/manutenção de naves e cadastro/consulta de humanos | Gestor e Supervisor, conforme especificação de referência. |
| Registrar pesquisa pré-missão | Pesquisador; avaliação por Gestor/Supervisor. |
| Definir missão e informar término | Gestor citado explicitamente; equivalência do Supervisor em OPEN-017. |
| Remarcar missão Adiada | Gestor e Supervisor. |
| Analisar morte / registrar resultado | Supervisor / Gestor. |
| Registrar/alterar dados científicos | Cientista; não estender edição científica aos administradores. |
| Consultar dados científicos | Cientista, Gestor e Supervisor. |
| Declarar obsolescência científica | Gestor e Supervisor. |
| Consultar / alterar histórico | Todos os funcionários / Gestor e Supervisor. |
| Consultar auditoria de alterações | Gestor e Supervisor; consulta registrada. |
| Editar/excluir manualmente auditoria de alterações | Nenhum perfil. |

## 12. Integrações e notificações

- **AlienZap:** processo anterior substituído; não há migração ou integração definida.
- **Área 51:** excluída expressamente.
- **E-mail:** FR-009 prevê envio de alerta crítico de bloqueio a Gestor/Supervisor, além do alerta no SGA. Destinatários operacionais e falhas em OPEN-021; provedor/tecnologia não definidos.
- **Notificações de missão:** internas, para funcionários envolvidos. Eventos relevantes em OPEN-012.
- Não há integração definida de folha salarial; o registro de punição não implica aplicação automática de desconto.

## 13. Decisões reaproveitadas do Discovery de referência

| ID | Decisão |
|---|---|
| DEC-001 | Cancelamento é definitivo e não permite reativação/reagendamento, substituindo a regra anterior que permitia reagendamento após cancelamento por indisponibilidade. |
| DEC-002 | Retorno inadequado e morte são ocorrências/exceções operacionais durante/depois da execução; não equivalem à relevância global na avaliação pré-missão. |
| DEC-003 | Notificações de missão são internas ao SGA no escopo acadêmico. |
| DEC-004 | Conflito de funcionários é definido pelo intervalo entre início e término da missão. |
| DEC-005 | A nave parte e retorna ao Estacionamento Alien; autonomia considera o percurso completo. |
| DEC-006 | Na reativação de funcionário são criadas novas credenciais; credenciais iniciais podem ser definidas por Gestor/Supervisor. |
| DEC-007 | A consolidação mantém apenas requisitos definidos; decisões técnicas de implementação ficam fora do Discovery. |

Além dessas decisões: login + senha; login único; credenciais iniciais administrativas; cinco falhas consecutivas bloqueiam por quinze minutos ou até desbloqueio aprovado, o que ocorrer primeiro; retenções de 2 e 6 meses. Origem: FR-005 a FR-011 e FR-085/086.

## 14. Questões abertas

Preservadas por rastreabilidade. Não é necessário reiniciar uma entrevista para utilizar os itens já definidos; as lacunas devem ser resolvidas antes da implementação dos comportamentos afetados.

| ID | Questão | Situação |
|---|---|---|
| OPEN-001 | Não foi definido um estado específico da missão durante a análise de morte. Não criar novo status sem decisão. | Aberta para refinamento. |
| OPEN-002 | “Nova advertência em dobro” não possui fórmula numérica detalhada. | Aberta para refinamento. |
| OPEN-003 | Auditoria de exclusão de dados científicos não foi detalhada; permanece a decisão explícita de não manter registro específico da exclusão. | Aberta para refinamento. |
| OPEN-004 | NFR-003 não possui métrica verificável para “prevenção contra perda ou alteração indevida”. Definir critério mensurável antes de considerar o NFR plenamente especificado. | Aberta para refinamento. |
| OPEN-005 | FR-013 usa “final do dia de trabalho”, mas não define horário ou regra objetiva para encerramento automático da sessão. | Aberta para refinamento. |
| OPEN-006 | FR-079 usa “imediatamente” para exclusão de dados obsoletos, sem limite temporal verificável. | Aberta para refinamento. |
| OPEN-007 | O levantamento não definiu claramente a duração de uma missão, embora o conflito de funcionários use o intervalo entre início e término. | Parcialmente definida; ver DEC-004/005 e histórias. |
| OPEN-008 | O levantamento não definiu regra operacional para determinar disponibilidade de funcionário além da condição de ativo/inativo. | Aberta para refinamento. |
| OPEN-009 | O levantamento não definiu como medir quilometragem/autonomia da nave nem a unidade/critério operacional além do valor cadastrado. | Parcialmente definida; ver DEC-004/005 e histórias. |
| OPEN-010 | O levantamento não definiu fluxo formal de etapas/status para o progresso da pesquisa científica. | Sem workflow adicional definido; não acrescentar funcionalidade. |
| OPEN-011 | O levantamento não definiu fórmula/critério para calcular “locais mais calmos” na pesquisa pré-missão. | Aberta para refinamento. |
| OPEN-012 | O levantamento não detalhou quais mudanças de missão são “relevantes” para disparo de notificações internas. | Aberta para refinamento. |
| OPEN-013 | O tratamento de punições por falha atribuível em caso de morte não define critérios objetivos de julgamento. | Aberta para refinamento. |
| OPEN-014 | O termo “consequência de saúde” no retorno inadequado não foi operacionalizado em critérios de classificação. | Aberta para refinamento. |
| OPEN-015 | O levantamento contém terminologia variável para a função operacional: “Abduzidor” no levantamento consolidado e “Abdutor” no Documento Base. A terminologia vigente do consolidado é “Abduzidor”. | Resolvida na fonte: adotar Abduzidor. |
| OPEN-016 | Delimitar o histórico geral diante dos dados científicos e da auditoria restritos. | Aberta para refinamento. |
| OPEN-017 | Explicitar a abrangência dos poderes iguais de Gestor e Supervisor. | Aberta para refinamento. |
| OPEN-018 | Definir retorno e encerramento em missões com vários humanos. | Aberta para refinamento. |
| OPEN-019 | Tratar indisponibilidade surgida depois do agendamento. | Aberta para refinamento. |
| OPEN-020 | Detalhar a sequência de tentativas de autenticação. | Aberta para refinamento. |
| OPEN-021 | Detalhar alerta crítico por e-mail e dentro do SGA. | Aberta para refinamento. |
| OPEN-022 | Completar o procedimento de troca e recuperação de senha. | Aberta para refinamento. |
| OPEN-023 | Definir validações dos dados cadastrais e científicos. | Aberta para refinamento. |
| OPEN-024 | Definir fronteiras temporais e numéricas do agendamento. | Aberta para refinamento. |
| OPEN-025 | Definir suficiência da pesquisa em missões com vários humanos. | Aberta para refinamento. |
| OPEN-026 | Definir cancelamento por relevância global antes do agendamento. | Aberta para refinamento. |
| OPEN-027 | Definir referência temporal e início automático após interrupção. | Aberta para refinamento. |
| OPEN-028 | Completar transições permitidas e remarcação. | Aberta para refinamento. |
| OPEN-029 | Completar contagem de advertências e punição salarial. | Aberta para refinamento. |
| OPEN-030 | Delimitar exclusão científica e dados preservados em auditoria. | Aberta para refinamento. |
| OPEN-031 | Detalhar retenção e expiração de auditoria. | Aberta para refinamento. |
| OPEN-032 | Definir quais alterações são relevantes para auditoria. | Aberta para refinamento. |
| OPEN-033 | Tornar verificável a disponibilidade 24×7. | Aberta para refinamento. |

## 15. Revisão de consistência

- Cancelamento definitivo preservado; apenas Adiada admite nova data.
- Exceção pré-missão de relevância global separada de morte e retorno inadequado durante/depois da execução.
- Histórico operacional editável separado da auditoria imutável.
- Consulta geral ao histórico não resolve nem amplia acesso aos dados científicos restritos; OPEN-016.
- Obsolescência científica e preservação de valores em auditoria precisam de delimitação; OPEN-003/030.
- Poderes administrativos iguais convivem com responsabilidades específicas e com a exclusividade de alteração científica; OPEN-017.
- Advertência em dobro e punição salarial não receberam fórmulas inventadas; OPEN-002/029.
- FR-018/088, FR-061/084 e FR-066/070 agrupados por comportamento, mantendo todos os IDs.

## 16. Backlog e critérios para continuidade

Esta versão organiza **7 épicos, 16 features, 30 histórias e 98 critérios de aceitação**, com cobertura dos 88 FR de referência. Há 1 história Ready para revisão e 29 em Refining devido às pendências específicas. Ready não significa código entregue nem validação final do professor.

Dependências centrais: cadastros → pesquisa → avaliação → planejamento → validação → execução → retorno/conclusão. Autenticação/permissões são transversais; auditoria acompanha os eventos definidos. Pesquisa científica depende de abdução realizada.

A etapa pode seguir para revisão acadêmica com pendências visíveis. Antes de implementar uma história, confirmar sua prioridade, resolver OPEN que impeça teste e conferir os critérios de aceitação. Não foi declarada conclusão integral de todos os pontos de Discovery.

