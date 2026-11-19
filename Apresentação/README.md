<div align="center">

# UDF PARKING
### Sua chegada já começa mais tranquila.

**Menos voltas. Mais planejamento. Cuidado no caminho.**

Projeto acadêmico de Engenharia de Software · Análise e Projeto de Sistemas · UDF

[**🎨 Explorar o novo Figma**](https://www.figma.com/design/8sZfS0XjwaMhVcZYGXSvJT/UDF-PARKING?node-id=17-702) · [**🌐 Abrir a maquete 3D**](https://udf-parking.vercel.app/) · [**📽️ Apresentação**](UDF_Parking_Apresentacao.pptx) · [**▶️ Vídeo**](UDF_Parking_Video.mp4)
 [**🌐 Abrir Documentação**](https://anahonorato.github.io/APS/)
</div>

---

## O projeto em 30 segundos

> O **UDF Parking** propõe reunir disponibilidade de vagas, opções de planos e benefícios noturnos em uma experiência simples para os estudantes da UDF. A ideia é ajudar o aluno a planejar a ida à faculdade, perder menos tempo procurando estacionamento e reduzir a necessidade de estacionar longe, especialmente à noite.

Esta pasta reúne os materiais para apresentar a proposta e demonstrar seus protótipos.

## O problema que queremos resolver

A experiência do aluno começa antes de entrar na sala de aula.

| Dificuldade | Resposta proposta |
| :--- | :--- |
| Sair sem saber se encontrará vaga | Consultar a disponibilidade antes do deslocamento |
| Perder tempo procurando onde estacionar | Visualizar setores e a situação das vagas |
| Pagar diárias com frequência | Comparar planos mensais, bimestrais e semestrais |
| Estacionar longe e caminhar à noite | Incentivar o uso do estacionamento próximo, com benefícios noturnos |

**Público principal:** estudantes da UDF que utilizam carro, com atenção especial ao período noturno.

## Quatro telas. Uma experiência conectada.

O protótipo mobile foi atualizado com uma identidade visual mais expressiva: **azul-noturno, vermelho UDF, tons claros e verde para disponibilidade**. Títulos, números e ações têm hierarquia própria para facilitar a leitura.

| Tela | O que apresenta | O que demonstrar |
| :--- | :--- | :--- |
| **01 · Início** | Saudação, disponibilidade geral e resumo dos setores | Como o aluno encontra a informação principal rapidamente |
| **02 · Mapa de vagas** | Mapa esquemático do setor A, vagas identificadas e detalhe de uma vaga acessível | Como ocupação e acessibilidade são informações distintas |
| **03 · Planos e tarifas** | Diária e propostas de planos mensal, bimestral e semestral | Como comparar períodos e valores equivalentes por mês |
| **04 · Cuidado noturno** | Descontos para estudantes e proposta de isenção noturna para mulheres | Como custo e deslocamento noturno fazem parte do problema |

A nova versão contém **quatro telas, componentes reutilizáveis e 17 conexões de navegação**, com transições suaves. A versão original foi mantida no mesmo arquivo para comparação.

### Teste o protótipo

1. [Abra a versão 02 no Figma](https://www.figma.com/design/8sZfS0XjwaMhVcZYGXSvJT/UDF-PARKING?node-id=17-702).
2. Selecione a tela **“01 • Início”**.
3. Clique em **▶ Apresentar**.
4. Use os botões e a navegação inferior para explorar **Início → Vagas → Planos → Cuidado**.

O fluxo demonstra a navegação entre telas. A consulta de vagas não equivale a uma reserva.

## Cuidado no caminho

A proposta considera a **segurança de homens e mulheres**, buscando reduzir a necessidade de realizar trajetos externos longos a pé no período noturno.

Dois benefícios são apresentados para avaliação:

- **Descontos noturnos para estudantes**, como incentivo ao uso do estacionamento próximo à instituição.
- **Isenção da taxa de estacionamento à noite especificamente para mulheres**, como medida proposta de apoio ao deslocamento noturno.

Esses benefícios dependem de avaliação de viabilidade e aprovação da UDF e da administração do estacionamento. Não representam políticas já implantadas nem uma garantia de segurança.

## Da interface à maquete 3D

O Figma apresenta a experiência mobile. A maquete permite explorar uma demonstração espacial do estacionamento, consultar vagas simuladas e observar a movimentação dos veículos.

| Material | Papel no projeto |
| :--- | :--- |
| **Figma** | Telas, identidade visual, componentes e navegação |
| **Maquete 3D** | Exploração visual do campus e simulação do estacionamento |
| **MoSCoW** | Priorização das funcionalidades |
| **Lean Canvas** | Organização do problema, público e proposta de valor |
| **Diagramas UML** | Modelagem dos processos, estrutura e relacionamentos do sistema |

**Tecnologias da maquete:** Next.js, React, TypeScript, Three.js, WebGL, Canvas 2D, Tailwind CSS e CSS. A publicação utiliza Vercel.

[Explorar a maquete](https://udf-parking.vercel.app/) · [Conhecer sua construção](../ProjetoAPS/Maquete3D/Projeto3D.md)

## Materiais para apresentar

| Recurso | Acesso |
| :--- | :--- |
| Slides em PowerPoint | [UDF_Parking_Apresentacao.pptx](UDF_Parking_Apresentacao.pptx) |
| Vídeo do projeto | [UDF_Parking_Video.mp4](UDF_Parking_Video.mp4) |
| Figma — versão 02 | [Abrir as telas atualizadas](https://www.figma.com/design/8sZfS0XjwaMhVcZYGXSvJT/UDF-PARKING?node-id=17-702) |
| Maquete interativa | [Abrir UDF Parking](https://udf-parking.vercel.app/) |
| Visão geral do projeto | [Ler a proposta](../ProjetoAPS/README.md) |
| Requisitos | [Ficha de elicitação](../ProjetoAPS/Docs_Requisitos/Ficha-Elicitação-REQ-001.md) |
| Priorização MoSCoW | [Consultar a priorização](../ProjetoAPS/MoSCoW.md) |
| Lean Canvas | [Abrir os modelos](../Unidade4/ModelagemSistemas/) |
| Modelagem UML | [Consultar os diagramas](../Unidade4/DocumentaçãoUML/) |
| Atividades e objetos — explicação e fontes | [Ler a documentação](../uml/README.md) |

### Roteiro sugerido · 5 minutos

| Tempo | Foco | Mensagem principal |
| :--- | :--- | :--- |
| **0:00–0:45** | Problema | O aluno pode chegar sem saber onde estacionar |
| **0:45–1:30** | Proposta | Reunir vagas, custos e benefícios em uma experiência simples |
| **1:30–3:00** | Demonstração | Percorrer as quatro telas do Figma e mostrar a maquete |
| **3:00–4:00** | Diferenciais | Explicar planos e benefícios noturnos propostos |
| **4:00–5:00** | Escopo e próximos passos | Apresentar os limites da demonstração e a necessidade de validação |

> **Sugestão de abertura:** “Antes de chegar à aula, o estudante já precisa tomar uma decisão: onde vai estacionar? O UDF Parking começa a resolver essa incerteza antes mesmo de ele sair.”

## O que está demonstrado — e o que ainda é proposta

| Situação | Escopo |
| :--- | :--- |
| **Demonstrado** | Interface mobile, navegação entre telas, maquete interativa e disponibilidade simulada |
| **Proposto** | Planos com desconto, benefícios noturnos e isenção noturna para mulheres |
| **Próximos passos** | Validar a experiência com estudantes, avaliar viabilidade com os responsáveis e estudar a obtenção de dados reais |

> [!IMPORTANT]
> **Este é um projeto acadêmico.** Ocupação, preços e percursos apresentados são demonstrativos. O protótipo não realiza reservas, pagamentos ou monitoramento real do estacionamento. Os valores exibidos não são uma tabela oficial da UDF.

## Equipe

[Ana Luísa](https://github.com/anahonorato) ·
[Gabriel Rufino](https://github.com/RufinoX12) ·
[João Paulo Ribeiro](https://github.com/jhonwayne07) ·
[Pietro Vianna](https://github.com/pietroviannadeveloper) ·
[Derik Noronha](https://github.com/Derikcrash) ·
[Matheus Henrique](https://github.com/mhenriqueazevedo-create)

---

<div align="center">

**UDF Parking**  
Planejar a chegada. Cuidar do caminho.

[Voltar ao repositório](../README.md)

</div>

