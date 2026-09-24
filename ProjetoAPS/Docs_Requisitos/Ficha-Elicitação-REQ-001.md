# Ficha de Elicitação de Requisitos

**Curso:** Engenharia de Software  
**Disciplina:** Análise e Projeto de Sistemas  
**Instituição:** UDF Centro Universitário  
**Grupo/integrantes:**  [Ana Luísa](https://github.com/anahonorato), [Gabriel Rufino](https://github.com/RufinoX12), [João Paulo Ribeiro](https://github.com/jhonwayne07) |
| 4 | [Pietro Vianna](https://github.com/pietroviannadeveloper) |
| 5 | [Derik Noronha](https://github.com/Derikcrash) |
| 6 | [Matheus Henrique](https://github.com/mhenriqueazevedo-create) |
  
**Turma:** D2 - Engenharia de Software  **Data:** 24/09/2026  **Versão:** 1.0

## 1. Identificação do projeto

| Campo | Preenchimento |
|---|---|
| Nome do projeto | UDF Parking — Sistema de Apoio ao Estacionamento da UDF |
| Objetivo do projeto | Os estudantes da UDF não conseguem saber antecipadamente se existem vagas no estacionamento, o que causa atrasos, perda de tempo, circulação desnecessária e a necessidade de estacionar longe da instituição. Além disso, o pagamento é feito por diária, sem planos adequados para usuários frequentes, e estacionar longe à noite aumenta a exposição de homens e mulheres no trajeto a pé. **Resultado esperado:** facilitar o planejamento do deslocamento, oferecendo informações sobre vagas, preços, planos e benefícios, para reduzir atrasos e custos e tornar os deslocamentos mais seguros, especialmente no período noturno. |
| Contexto e escopo | Sistema que permite ao estudante consultar a disponibilidade de vagas do estacionamento da UDF antes de se deslocar, reunindo também preços, horários, descontos noturnos, planos mensal, bimestral e semestral e a proposta de isenção noturna para mulheres. Nesta etapa, o trabalho se concentra na análise do problema e dos requisitos: não estão incluídos sensores, APIs, cancelas nem o desenvolvimento completo do sistema. |

## 2. Stakeholder e fonte

| Campo | Preenchimento |
|---|---|
| Stakeholder (nome ou papel) | ST01 — Alunos da UDF que utilizam carro, principalmente no período noturno (stakeholder principal). |
| Relação com o projeto | Usuário principal: são os diretamente afetados pela falta de informação sobre vagas, pelo pagamento recorrente de diárias e pela exposição ao estacionar longe da instituição à noite. Influência: alta. |
| Contato ou setor (se aplicável) | Corpo discente da UDF (estudantes que vão de carro; ênfase no período noturno). |
| Técnica e data da elicitação | Observação do problema; setembro de 2026. |
| Responsável pelo registro | Grupo do projeto (integrantes listados no cabeçalho). |

## 3. Requisito elicitado

| Campo | Preenchimento |
|---|---|
| ID do requisito | REQ-001 (corresponde ao RF01 do levantamento do grupo). |
| Necessidade relatada pelo stakeholder | N01 — “Consultar vagas antes do deslocamento”: o estudante vai até a UDF sem saber se encontrará vaga e só descobre a lotação ao chegar ao estacionamento. |
| Descrição consolidada | O sistema deve permitir ao estudante consultar a disponibilidade de vagas do estacionamento da UDF antes de se deslocar até a instituição, sem que ele precise estar no local. |
| Justificativa ou benefício esperado | É a função central do sistema. Evita atrasos, perda de tempo procurando vaga, circulação desnecessária e a necessidade de estacionar longe da UDF, especialmente à noite. |
| Tipo | Funcional. |
| Dependências ou dúvidas | 1) A fonte confiável dos dados de ocupação ainda não foi definida (RES03), e esta etapa não prevê sensores, APIs ou cancelas (RES01).<br>2) A frequência de atualização dos dados ainda precisa ser definida no estudo de viabilidade.<br>3) Os critérios de “muitas vagas”, “poucas vagas” e “lotado” dependem da gestão do estacionamento (ver RF02).<br>4) Ainda não está definido se a consulta exigirá login ou será aberta a todos (professores, funcionários e visitantes, ST05, também poderiam consultar).<br>5) Requisitos de qualidade relacionados: RQ01 (desempenho), RQ03 (usabilidade), RQ04 (última atualização) e RQ05 (compatibilidade). |

## 4. Regras de negócio

| ID | Regra de negócio relacionada | Fonte ou responsável pela validação |
|---|---|---|
| RN-001 | A situação do estacionamento deve ser apresentada como “muitas vagas”, “poucas vagas” ou “lotado”, conforme critérios definidos pela gestão do estacionamento. | Gestão do estacionamento (ST04) |

## 5. Prioridade

**Classificação MoSCoW (marque uma):** [x] Must have (essencial)  [ ] Should have (importante)  [ ] Could have (desejável)  [ ] Won't have nesta versão (fora do escopo atual)

**Justificativa da prioridade:** Representa a função principal do sistema e é o primeiro item da primeira versão. Sem ela, o estudante continua descobrindo a lotação apenas ao chegar à UDF.

## 6. Critérios de aceitação

Escreva condições verificáveis que permitam decidir se o requisito foi atendido.

| ID | Dado/Quando | Então (resultado esperado) | Evidência ou forma de verificação |
|---|---|---|---|
| CA-01 | Dado um estudante que ainda não chegou à UDF, quando ele acessar o sistema e solicitar a consulta de vagas | Então o sistema apresenta a disponibilidade atual de vagas do estacionamento, sem exigir que o estudante esteja no local. | Teste funcional com acesso externo à UDF, em computador e em celular. |
| CA-02 | Dado um estudante que acabou de acessar o sistema, quando ele buscar a disponibilidade de vagas | Então ele chega ao resultado em até três interações (RQ03). | Teste de usabilidade com estudantes, contando as interações até o resultado. |
| CA-03 | Dado o sistema em condições normais de uso, quando o estudante solicitar a consulta | Então o resultado é exibido em até 2 segundos para 95% das requisições (RQ01). | Teste de desempenho com medição do tempo de resposta. |
| CA-04 | Dado que a consulta de vagas foi realizada, quando o resultado for exibido | Então o sistema mostra também o horário da última atualização das informações de ocupação (RQ04). | Comparação entre o horário exibido e o registro da última atualização dos dados. |

## 7. Validação e rastreabilidade

| Campo | Preenchimento |
|---|---|
| Situação | [x] Pendente de validação  [ ] Validado  [ ] Necessita revisão |
| Validado por / data | Ainda não validado. A revisão por pares e a validação com o stakeholder estão pendentes. |
| Observações e decisões | Requisito classificado como Must have e incluído na primeira versão (ordem 1). Pendências levantadas na revisão: definir o intervalo de atualização dos dados (RQ04) e os percentuais de “muitas vagas / poucas vagas / lotado” (RF02). |
| Links relacionados | Rastreabilidade: N01 → ST01 → REQ-001 (RF01), relacionado a RF08, RQ01, RQ03, RQ04 e RQ05.<br>[Board do projeto no Miro](https://miro.com/welcomeonboard/Y2RxT2ZYT09JNHgzcTVMR096YklKbEVCSkdabXh5d2hpTU9xR0M2VGUzWGtJSytPOUEwK0R5VkVBb2k4ZmR6Nm8rclFYMm56RmxlcUQ2UjZkWjU3QlZRczg2eVFCcHdMdFpkNkhUcjBrenBjdEFDODRVZk95eXZmWDZURWlwbS90R2lncW1vRmFBVnlLcVJzTmdFdlNRPT0hdjE=?share_link_id=66753103227)<br>[Repositório GitHub — APS](https://github.com/anahonorato/APS) |
