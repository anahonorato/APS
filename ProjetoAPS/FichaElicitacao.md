# Ficha de Elicitação de Requisitos

**Curso:** Engenharia de Software  
**Disciplina:** Análise e Projeto de Sistemas  
**Instituição:** UDF Centro Universitário  
**Grupo/integrantes:** Ana Luísa Honorato, Gabriel Rufino, João Paulo, Pietro Vianna, Derik Noronha, Matheus Henrique.  
**Turma:** D2 - Engenharia de Software  **Data:** 24/09/2026 **Versão:** 1.0

> Preencha uma ficha para cada requisito identificado. Registre a necessidade na linguagem do stakeholder e esclareça termos ambíguos antes de validar a ficha com ele.

## 1. Identificação do projeto

| Campo | Preenchimento |
|---|---|
| Nome do projeto | UDF Parking |
| Objetivo do projeto | Os estudantes da UDF não conseguem saber antecipadamente se existem vagas disponíveis no estacionamento. Essa falta de informação pode causar atrasos, perda de tempo, circulação desnecessária e a necessidade de estacionar longe da instituição. Além disso, o pagamento é realizado por diária, sem planos adequados para usuários frequentes. No período noturno, estacionar longe também aumenta a exposição de homens e mulheres durante o trajeto a pé, tornando a segurança uma preocupação relevante. |
| Contexto e escopo | Proposta de um sistema que permita aos estudantes consultar a disponibilidade de vagas no estacionamento da UDF antes do deslocamento. A solução também reunirá informações sobre preços, horários, descontos noturnos, planos mensais, bimestrais e semestrais e a proposta de isenção noturna para mulheres, contribuindo para o planejamento, a redução de custos e a segurança dos estudantes.

 |

## 2. Stakeholder e fonte

| Campo | Preenchimento |
|---|---|
| ID | Stakeholder | Papel | Necessidade/Interesse | Influência |
|---|---|---|---|---|
| ST01 | Alunos que utilizam carro | Usuários principais | Consultar vagas, preços e benefícios | Alta |
| ST02 | Alunas do período noturno | Usuárias beneficiadas pela proposta de isenção | Utilizar uma área próxima e reduzir trajetos noturnos a pé | Alta |
| ST03 | Administração da UDF | Responsável institucional | Avaliar a viabilidade e definir as políticas | Alta |
| ST04 | Gestão do estacionamento | Responsável operacional | Informar ocupação, preços, horários e regras | Alta |
| ST05 | Professores, funcionários e visitantes | Usuários secundários | Consultar a disponibilidade do estacionamento | Média |

| Técnica e data da Elicitação | Observação setembro de 2026. |
| Responsável pelo registro | Colaboradores do projeto |

## 3. Requisito elicitado

. Necessidades Identificadas

| ID | Stakeholder | Necessidade identificada | Problema relacionado |
|---|---|---|---|
| N01 | Alunos | Consultar vagas antes do deslocamento | Falta de informação antecipada |
| N02 | Alunos | Visualizar o nível de lotação por setor | Tempo perdido procurando vagas |
| N03 | Alunos | Consultar preços e horários | Informações descentralizadas |
| N04 | Alunos frequentes | Ter alternativas ao pagamento diário | Custo recorrente elevado |
| N05 | Alunos do período noturno | Obter desconto noturno | Custo do estacionamento à noite |
| N06 | Mulheres do período noturno | Consultar as condições da proposta de isenção | Segurança e trajetos externos noturnos |
| N07 | Homens e mulheres | Consultar orientações e acessos mais seguros | Exposição durante o deslocamento noturno |
| N08 | Administração | Acompanhar a utilização do estacionamento | Falta de informações consolidadas |

---

. Requisitos Funcionais

## Requisitos Funcionais do Projeto

| ID | Requisito funcional | Stakeholder/Fonte | Necessidade | Prioridade |
|---|---|---|---|---|
| RF01 | O sistema deve permitir a consulta da disponibilidade de vagas antes do deslocamento até a UDF. | ST01 | N01 | Must Have |
| RF02 | O sistema deve apresentar a ocupação por setor e indicar se há muitas vagas, poucas vagas ou lotação. | ST01 e ST04 | N02 | Must Have |
| RF03 | O sistema deve apresentar preços, horários e formas de pagamento do estacionamento. | ST01 e ST04 | N03 | Must Have |
| RF04 | O sistema deve apresentar e comparar os planos mensal, bimestral e semestral com o pagamento por diária. | ST01 e ST03 | N04 | Should Have |
| RF05 | O sistema deve informar os descontos disponíveis para estudantes no período noturno. | ST01 e ST03 | N05 | Should Have |
| RF06 | O sistema deve informar os critérios da proposta de isenção noturna especificamente para mulheres. | ST02 e ST03 | N06 | Should Have |
| RF07 | O sistema deve apresentar orientações de segurança e indicar acessos ou trajetos mais seguros no período noturno. | ST01 e ST02 | N07 | Should Have |
| RF08 | O sistema deve permitir o recebimento de notificações quando o estacionamento estiver próximo da lotação ou lotado. | ST01 | N01 e N02 | Could Have |

---

. Requisitos de Qualidade

## Requisitos de Qualidade do Projeto

| ID | Característica | Requisito | Como será verificado? |
|---|---|---|---|
| RQ01 | Desempenho | O sistema deve apresentar o resultado das consultas em até 2 segundos para 95% das requisições em condições normais de uso. | Testes de desempenho e medição do tempo de resposta |
| RQ02 | Segurança | O sistema deve proteger dados pessoais e acadêmicos e limitar o acesso às informações de benefícios. | Testes de acesso e verificação das permissões |
| RQ03 | Usabilidade | Um estudante deve conseguir consultar a disponibilidade de vagas em até três interações após acessar o sistema. | Testes de usabilidade com estudantes |
| RQ04 | Confiabilidade | O sistema deve mostrar o horário da última atualização das informações de ocupação. | Comparação entre o horário informado e o registro da atualização |
| RQ05 | Compatibilidade | O sistema deve funcionar em navegadores atuais de computadores e dispositivos móveis. | Testes nos principais navegadores e tamanhos de tela |

## 4. Regras de negócio

| ID | Regra de negócio relacionada | Fonte ou responsável pela validação |
| ID | Regra de negócio | Fonte |
|---|---|---|
| RN01 | Os planos e descontos destinados a estudantes somente poderão ser concedidos mediante validação do vínculo acadêmico ativo. | Administração da UDF |
| RN02 | A proposta de isenção noturna para mulheres deverá ser aplicada apenas no período e nas condições definidos e aprovados pela UDF. | Administração da UDF |
| RN03 | A situação do estacionamento deverá ser apresentada como “muitas vagas”, “poucas vagas” ou “lotado”, conforme critérios definidos pela gestão do estacionamento. | Gestão do estacionamento |

## 5. Prioridade

| ID | Requisito | MoSCoW | Justificativa |
|---|---|---|---|
| RF01 | Consultar a disponibilidade de vagas | M | Representa a função principal do sistema |
| RF02 | Visualizar a ocupação e o status por setor | M | Permite compreender rapidamente a situação do estacionamento |
| RF03 | Consultar preços, horários e pagamentos | M | Reúne informações essenciais para a decisão do estudante |
| RF04 | Consultar e comparar planos | S | Reduz custos, mas depende de aprovação financeira |
| RF05 | Consultar descontos noturnos | S | Possui alto valor, mas depende de uma política institucional |
| RF06 | Consultar a isenção noturna para mulheres | S | Contribui para a segurança, mas depende de análise e aprovação |
| RF07 | Consultar orientações e trajetos mais seguros | S | Complementa a solução e fortalece a segurança noturna |
| RF08 | Receber notificações de lotação | C | Melhora a experiência, mas não é necessária para a primeira versão |
| RQ01 | Responder às consultas em até 2 segundos | M | Evita espera durante a tomada de decisão |
| RQ02 | Proteger dados pessoais e acadêmicos | M | É necessário proteger as informações utilizadas pelo sistema |
| RQ03 | Permitir a consulta em até três interações | M | A consulta precisa ser simples e rápida |
| RQ04 | Informar o horário da última atualização | M | Evita que o usuário tome decisões com dados desatualizados |
| RQ05 | Funcionar em computadores e celulares | M | Os estudantes utilizarão principalmente dispositivos móveis |

## 6. Critérios de aceitação

Escreva condições verificáveis que permitam decidir se o requisito foi atendido.

| Ordem | ID | Requisito | Por que deve estar na primeira versão? |
|---:|---|---|---|
| 1 | RF01 | Consultar disponibilidade de vagas | É a principal finalidade da solução |
| 2 | RF02 | Visualizar ocupação e status por setor | Transforma os dados em uma informação clara |
| 3 | RF03 | Consultar preços e horários | Ajuda o aluno a decidir se utilizará o estacionamento |
| 4 | RQ03 | Consulta simples e rápida | Garante que a solução seja fácil de utilizar |
| 5 | RQ04 | Informar a última atualização | Aumenta a confiança nas informações apresentadas |

## 7. Validação e rastreabilidade

| Necessidade | Stakeholder | Requisito(s) relacionado(s) |
|---|---|---|
| N01 | ST01 | RF01, RF08, RQ01 e RQ04 |
| N02 | ST01 e ST04 | RF02, RF08 e RQ04 |
| N03 | ST01 e ST04 | RF03 |
| N04 | ST01 e ST03 | RF04 |
| N05 | ST01 e ST03 | RF05 |
| N06 | ST02 e ST03 | RF06 e RQ02 |
| N07 | ST01 e ST02 | RF07 e RQ03 |
| N08 | ST03 e ST04 | RF02 e RQ04 |
## Exemplo breve (fictício)

> Nosso projeto pretende facilitar o planejamento do deslocamento dos estudantes da UDF, oferecendo informações sobre vagas, preços, planos e benefícios do estacionamento, contribuindo para a redução de atrasos e custos e para deslocamentos mais seguros, especialmente no período noturno. > Os estudantes da UDF não conseguem saber antecipadamente se existem vagas disponíveis no estacionamento. Essa falta de informação pode causar atrasos, perda de tempo, circulação desnecessária e a necessidade de estacionar longe da instituição.
> Além disso, o pagamento é realizado por diária, sem planos adequados para usuários frequentes. No período noturno, estacionar longe também aumenta a exposição de homens e mulheres durante o trajeto a pé, tornando a segurança uma preocupação relevante. Stakeholder:> Alunos da UDF que utilizam carro, principalmente no período noturno.Por que ele foi considerado o principal stakeholder Os alunos são os usuários diretamente afetados pela falta de informações sobre vagas e pelo pagamento recorrente de diárias. São eles que enfrentam atrasos, perda de tempo, custos elevados e maior exposição ao estacionar longe da instituição durante a noite.
