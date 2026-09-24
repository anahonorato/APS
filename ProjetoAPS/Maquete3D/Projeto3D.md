# 🅿️ UDF Parking — Campus 3D

<p align="center">
  <strong>Protótipo interativo para visualização, planejamento e simulação do estacionamento universitário.</strong>
</p>

<p align="center">
  Engenharia de Software · Análise e Projeto de Sistemas — UDF
</p>

<p align="center">
  <a href="https://udf-parking.vercel.app/">
    <strong>🌐 Acessar o protótipo publicado</strong>
  </a>
  &nbsp;•&nbsp;
  <a href="https://github.com/anahonorato/APS">
    <strong>📂 Repositório</strong>
  </a>
</p>

---

## 📌 Sobre o projeto

O **UDF Parking — Campus 3D** é uma prova de conceito desenvolvida para investigar como uma experiência visual e interativa pode facilitar o planejamento do uso do estacionamento universitário.

A solução combina uma **Recriação fictícia demaquete 3D do campus** com informações simuladas sobre:

* disponibilidade de vagas;
* planos de estacionamento;
* custos de utilização;
* benefícios noturnos;
* segurança no estacionamento.

O projeto aplica conceitos de **Análise e Projeto de Sistemas**, desenvolvimento front-end, modelagem 3D e experiência do usuário em uma interface responsiva e interativa.

> [!IMPORTANT]
> Este é um **protótipo acadêmico**.
> As vagas, preços, percursos e benefícios apresentados são demonstrativos.
>
> O sistema **não realiza reservas, pagamentos, monitoramento por sensores ou consulta de dados reais de ocupação**.

---

## 🎯 Problema

A incerteza sobre a disponibilidade de vagas pode dificultar o planejamento da ida à universidade.

Para usuários frequentes, o pagamento diário também pode representar um custo elevado ao longo do mês.

Durante o período noturno, além da disponibilidade de vagas, fatores relacionados à **segurança e previsibilidade do deslocamento** também se tornam relevantes.

---

## 💡 Proposta de solução

O protótipo apresenta uma experiência centralizada que permite:

* 🚗 consultar visualmente vagas disponíveis;
* 💳 comparar planos de estacionamento;
* 📉 visualizar descontos progressivos;
* 🌙 consultar benefícios para utilização no período noturno;
* 👩 visualizar a proposta de isenção noturna para mulheres;
* 🛡️ acompanhar um percurso ilustrativo de segurança dentro do estacionamento.

---

## ✨ Funcionalidades

### 🏫 Campus 3D

* Maquete tridimensional interativa;
* rotação da câmera;
* zoom;
* passeio automático;
* foco por setor;
* seleção de vagas diretamente pela cena.

### 🅿️ Estacionamento

* **72 vagas demonstrativas**;
* divisão entre os setores **A**, **B** e **Visitantes**;
* seleção pela maquete 3D;
* seleção por grade de vagas;
* indicação visual de disponibilidade.

### 📊 Simulação de ocupação

* atualização dinâmica das vagas;
* contadores de ocupação;
* alteração visual em tempo real;
* possibilidade de pausar a simulação.

### 💰 Comparação de planos

O usuário pode informar sua frequência estimada de utilização mensal e comparar diferentes opções:

* plano mensal;
* plano bimestral;
* plano semestral;
* utilização avulsa.

### 🌙 Modo Dia e Noite

A interface permite alternar entre diferentes condições de iluminação.

No modo noturno são modificados:

* iluminação da cena;
* materiais;
* aparência do campus;
* elementos relacionados à proposta de segurança.

### 🛡️ Segurança

A aba de segurança apresenta:

* percurso ilustrativo dentro do estacionamento;
* pontos de referência;
* benefícios noturnos propostos;
* destaque para iniciativas voltadas à segurança dos estudantes.

### ♿ Acessibilidade e compatibilidade

* Layout responsivo;
* suporte a diferentes tamanhos de tela;
* suporte à preferência `prefers-reduced-motion`;
* renderização alternativa em **Canvas 2D** quando WebGL não estiver disponível.

---

## 🎮 Como utilizar

Na página principal:

1. 🖱️ Explore o campus utilizando o mouse ou toque;
2. 🅿️ selecione uma vaga na maquete 3D ou na grade;
3. ☀️🌙 alterne entre os modos **Dia** e **Noite**;
4. 🚘 execute a simulação de ocupação;
5. 📅 informe sua frequência mensal de utilização;
6. 💰 compare os planos disponíveis;
7. 🛡️ acesse a área de segurança e benefícios noturnos.

---

## 🛠️ Tecnologias utilizadas

| Tecnologia         | Aplicação                               |
| ------------------ | --------------------------------------- |
| **Next.js 16**     | Estrutura principal da aplicação        |
| **React 19**       | Construção da interface interativa      |
| **TypeScript**     | Tipagem e organização da lógica         |
| **Three.js**       | Construção e renderização da maquete 3D |
| **WebGL**          | Renderização gráfica acelerada          |
| **Canvas 2D**      | Fallback para ambientes sem WebGL       |
| **Tailwind CSS 4** | Estilização e layout                    |
| **CSS**            | Estados visuais e ajustes específicos   |
| **shadcn/ui**      | Componentes e primitivas de interface   |
| **Lucide React**   | Ícones utilizados na aplicação          |
| **Figma**          | Prototipação e referência visual        |
| **Vercel**         | Hospedagem e publicação                 |

---

## 🧊 Construção da maquete 3D

A maquete foi construída diretamente em código utilizando **Three.js**.

As diferentes partes do campus são representadas através de geometrias tridimensionais, incluindo:

* prédios;
* telhados;
* janelas;
* vias;
* árvores;
* postes;
* veículos;
* vagas de estacionamento.

Os objetos da cena são organizados individualmente para permitir interações e atualizações durante a execução da aplicação.

---

### 🎥 Câmera e navegação

A aplicação utiliza uma câmera em perspectiva combinada com `OrbitControls`.

Isso permite:

* rotação ao redor da maquete;
* aproximação e afastamento;
* alteração do ponto de observação;
* navegação livre pelo cenário.

---

### 🎯 Seleção de vagas

A interação com objetos utiliza **raycasting**.

A posição do cursor é convertida para as coordenadas da cena 3D, permitindo identificar qual objeto foi selecionado pelo usuário.

Esse mecanismo possibilita selecionar diretamente:

* vagas;
* veículos;
* elementos interativos da cena.

---

### 🎞️ Sistema de animação

O ciclo de renderização utiliza:

```javascript
requestAnimationFrame()
```

Ele é responsável por atualizar continuamente:

* câmera;
* veículos;
* animações;
* estados da simulação;
* transições visuais.

---

### 🌙 Iluminação dinâmica

Os modos **Dia** e **Noite** alteram propriedades da cena, incluindo:

* intensidade das luzes;
* materiais;
* cores;
* aparência geral do ambiente.

No modo noturno, elementos relacionados ao percurso de segurança recebem maior destaque visual.

---

### 🖼️ Fallback em Canvas 2D

Caso o navegador não consiga inicializar o **WebGL**, a aplicação utiliza um renderizador alternativo baseado em **Canvas 2D**.

As geometrias da cena são projetadas em duas dimensões para manter uma representação funcional do estacionamento.

O renderizador:

* acompanha automaticamente o tamanho do contêiner;
* mantém uma representação visual da cena;
* libera recursos gráficos durante a desmontagem dos componentes.

---

## 🗂️ Estrutura principal

```text
Projeto3D/
│
├── app/
│   ├── page.tsx
│   ├── scene.tsx
│   ├── software-renderer.ts
│   └── parking.css
│
├── components/
│   └── ui/
│
├── public/
│
├── package.json
├── tsconfig.json
└── vercel.json
```

### Responsabilidade dos principais arquivos

| Arquivo / Diretório        | Responsabilidade                                           |
| -------------------------- | ---------------------------------------------------------- |
| `app/page.tsx`             | Interface principal, vagas, simulação e cálculo dos planos |
| `app/scene.tsx`            | Construção e interação da cena Three.js                    |
| `app/software-renderer.ts` | Renderização alternativa em Canvas 2D                      |
| `app/parking.css`          | Identidade visual, estados e responsividade                |
| `components/ui/`           | Componentes reutilizáveis da interface                     |
| `vercel.json`              | Configuração de publicação na Vercel                       |

---

## ⚙️ Requisitos

Para executar o projeto localmente:

* **Node.js 22.13** ou superior;
* **npm**;
* navegador moderno;
* suporte a WebGL recomendado.

> Caso WebGL não esteja disponível, o projeto utiliza automaticamente sua alternativa em Canvas 2D.

---

## 🚀 Executando localmente

### 1. Clone o repositório

```bash
git clone https://github.com/anahonorato/APS.git
```

### 2. Entre no projeto

```bash
cd APS/Projeto3D
```

### 3. Instale as dependências

```bash
npm install
```

### 4. Inicie o ambiente de desenvolvimento

```bash
npm run dev
```

### 5. Abra no navegador

```text
http://localhost:3000
```

---

## 📦 Executando a versão de produção

Gere a build otimizada:

```bash
npm run build
```

Depois execute:

```bash
npm start
```

A aplicação estará disponível em:

```text
http://localhost:3000
```

---

## 🔗 Links do projeto

| Recurso                    | Link                                                             |
| -------------------------- | ---------------------------------------------------------------- |
| 🌐 **Protótipo publicado** | [udf-parking.vercel.app](https://udf-parking.vercel.app/)        |
| 💻 **Repositório GitHub**  | [github.com/anahonorato/APS](https://github.com/anahonorato/APS) |
| 🎨 **Protótipo no Figma**  | *Adicionar link*                                                 |
| 🗺️ **Board MoSCoW**       | *Adicionar link*                                                 |

---

## 📚 Escopo e limitações

O **UDF Parking — Campus 3D** representa uma solução conceitual e não possui integração com a infraestrutura real do estacionamento da UDF.

Os dados exibidos são exclusivamente demonstrativos e não devem ser utilizados para decisões reais relacionadas a:

* disponibilidade de vagas;
* pagamentos;
* deslocamento;
* segurança;
* acesso ao campus.

---

## 🔮 Possíveis evoluções

Como continuação do projeto, a solução poderia incorporar:

* 📡 sensores de ocupação em tempo real;
* 🔌 API de disponibilidade de vagas;
* 👤 autenticação de usuários;
* 📲 aplicativo mobile;
* 🎫 reserva antecipada de vagas;
* 💳 pagamentos digitais;
* 🔔 notificações de disponibilidade;
* ♿ dados oficiais de vagas acessíveis;
* 🛡️ integração com informações oficiais de segurança do campus;
* 📊 histórico e análise de ocupação;
* 🗺️ mapa mais detalhado do campus.

---

## 🎓 Contexto acadêmico

Projeto desenvolvido para a disciplina de **Análise e Projeto de Sistemas**, do curso de **Engenharia de Software da UDF**.

O objetivo é aplicar conceitos relacionados a:

* levantamento de requisitos;
* definição de escopo;
* prototipação;
* priorização de funcionalidades;
* experiência do usuário;
* modelagem de sistemas;
* desenvolvimento de interfaces.

---

## 📄 Licença

Este projeto foi desenvolvido para **fins acadêmicos**.

Consulte os responsáveis pelo repositório antes de reutilizar código, modelos, elementos gráficos ou materiais visuais em outros projetos.

---

<p align="center">
  <strong>UDF Parking — Campus 3D</strong><br>
  Engenharia de Software · UDF
</p>
