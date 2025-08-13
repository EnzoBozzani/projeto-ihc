# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **PESQUISA E IMPLEMENTAÇÃO DE PLATAFORMA PARA CRIAÇÃO DE FLUXOS MULTI-AGENT** sob orientação do Professor **Prof. Dr. Flavio Tonidandel** e desenvolvido pelos seguintes alunos:

-   Adriel Henrique Foppa Lima - 24.122.096-1
-   Alan Mantelatto Mlatisuma - 22.125.092-1
-   Enzo Bozzani Martins - 24.122.020-1
-   Igor Augusto Fiorini Rossi - 22.225.021-9

## Resumo

A aplicação é um webapp que tem como objetivo a criação de fluxos multi-agent baseados em LLMs (Large Language Models). Para a criação dos fluxos, são utilizadas algumas entidades principais:

-   **Agentes**: Modelos de inteligência artificial especializados em alguma tarefa. Os agentes podem ser criados utilizando diferentes modelos de linguagem e ferramentas (pré-definidas na plataforma), e especializados em uma das seguintes tarefas:
    -   Orquestração de agentes
    -   Extração de dados de documentos
    -   Acesso a banco de dados
    -   Pesquisa na Internet
    -   Criação de apresentações PowerPoint
    -   Comunicação externa por meio do envio de e-mails
-   **Recursos**: Recursos acoplados aos agentes no fluxo. São documentos, bancos de dados e e-mail que podem ser acessados e utilizados pelos modelos.
-   **Fluxos**: Abstrações para implementações de soluções utilizando os agentes e recursos. Por meio de uma interface de grafo, os agentes e recursos são combinados em formato de nós, e conectados por meio de arestas, que funcionam como a comunicação entre diferentes nós.

Ao oferecer interfaces para o gerenciamento dessas entidades, o webapp permite que seus usuários criem fluxos em que agentes baseados em modelos pequenos colaboram para resolver problemas complexos. A escolha por modelos pequenos se deve pelo seu baixo custo computacional (e consequentemente financeiro), se tornando uma opção viável para automatização de processos sem necessidade de alto aporte financeiro.

## Introdução
 
- **Apresente o propósito do produto ou serviço e quais são os principais benefícios que ele oferece aos usuários**: O serviço tem como propósito fornecer uma plataforma para criação de fluxos multi agentes baseados na colaboração entre modelos pequenos. Os fluxos podem ser modelados de maneira que se adequem ao propósito do usuário, que pode depois integrar tais fluxos em seus processos. 
- **Identifique os problemas ou necessidades que o produto ou serviço resolve ou satisfaz**: Hoje, muito se fala da insurgência dos modelos de linguagem e de agentes, mas existem poucas aplicações que abstraem os conceitos técnicos da criação desses agentes, e ainda menos aplicações que fornecem essa abstração por um custo baixo, visto que os LLMs normalmente exigem uma infraestrutura robusta. Por isso, a plataforma preenche esse espaço como centro de criação e aplicação de fluxos baseados em agentes que solucionam problemas complexos de maneira automatizada, eficiente e intuitiva.
- **Liste as características e funcionalidades do seu produto ou serviço de forma detalhada:** A ferramenta tem como funcionalidades principais gerenciamento (criação, visualização e remoção) de fluxos, agentes e recursos (documentos, bancos de dados e e-mail), além da edição de fluxo, onde o usuário conecta os agentes, ferramentas e recursos para montar suas soluções. Os agentes são definidos pela escolha de uma tarefa e modelo, além da possibilidade de acoplar um dos recursos dependendo da tarefa escolhida. As tarefas disponíveis na qual os agentes podem ser especializados são: Orquestração de agentes, Extração de dados de documentos, Acesso a banco de dados, Pesquisa na Internet, Criação de apresentações PowerPoint e Comunicação externa por meio do envio de e-mails. Ao agrupar diferentes agentes em um fluxo, o usuário pode criar as mais diversas automações a serem integradas em sua infraestrutura.
- **Liste as tecnologias e ferramentas computacionais que pretendem usar neste projeto (TCC)**: Python, LangChain, Ollama, Model Context Protocol (MCP), MongoDB, Neo4J, NextJS com TypeScript. 
- **Apresente o contexto de uso dessa aplicação. (“Usuários, tarefas, equipamentos (hardware, software e materiais) e o ambiente físico e social no qual um produto é usado.”)**: Os usuários são, principalmente, empresas que desejam incluir fluxos multi agentes em suas aplicações sem a necessidade de desenvolver código para isso, entretanto qualquer pessoa que busque uma ferramenta para criar fluxos pode usar a aplicação. A aplicação é feita para ser utilizada em qualquer dispositivo que tenha um navegador, podendo ser usada tanto em computadores quanto dispositivos móveis. Como os modelos são hospedados e os fluxos executados em nossa infraestrutura, não há necessidade de hardware potente por parte do usuário para a utilização. O ambiente físico e social é, primariamente, um ambiente corporativo em que os usuários busquem a utilização de múltiplos agentes em seus processos, sem a necessidade de escrever código para criar esses agentes e suas comunicações.

## Publico Alvo

- Determine qual o grupo específico de pessoas ou organizações para as quais este produto ou serviço é direcionado.
- Descreva as caracteristicas demográficas, comportamentais, psicográficas ou geográficas deste público alvo que o torna mais propenso a se interessar pelo que está sendo oferecido neste projeto ou serviço.

## Análise de concorrência

1. Identifique os principais concorrentes ou softwares mais utilizados pelo seu público-alvo.
2. Colete informações sobre os concorrentes selecionados.
3. Analise as características e funcionalidades dos concorrentes.
4. Avalie a experiência do usuário (UX).
5. Examine os preços e modelos de negócio.
6. Pesquisa de satisfação do cliente e opiniões.
7. Identifique padrões e tendências no mercado.
8. Elabore relatórios e sumarize os resultados.
9. Extraia pontos positivos e faça recomendações.

### Personas

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?

  - Persona primaira ...
  - Persona secundária ...
  - Outras personas ...

### Mapa de empatia

![Mapa de empatia](empatia.png)

- Determine o mapa de empatia[^1] de pelo menos uma persona primária e uma sercundária.
  - O que o usuário vê: aqui estamos falando do ambiente visual em que o usuário se encontra. Ou seja, o que ele efetivamente enxerga, as pessoas e objetos que estão ao seu redor. Isso ajuda a entender o contexto em que o usuário está inserido e as influências visuais que está recebendo.
  - O que o usuário ouve: neste quadrante, buscamos entender o que o usuário está ouvindo, os sons que o cercam e como eles influenciam suas ações.
  - O que o usuário diz e faz: aqui consideramos ações e comportamentos que o usuário apresenta durante sua interação com serviço ou poduto.
  - O que o usuário pensa e sente: neste quadrante, buscamos entender os pensamentos, sentimentos, emoções e percepções que o usuário tem em relação ao serviço ou poduto. Quais expectativas o usuário cria sobre o serviço ou poduto?
  Que tipo de serviço ou poduto mais agrada essa persona?
  - Dores: quando falamos sobre dores do usuário, estamos fazendo referência a quaisquer obstáculos, necessidades ou frustrações que o usuário possa experimentar ao tentar realizar uma tarefa ou alcançar um objetivo. Isso inclui, por exemplo, problemas de usabilidade, dificuldades de acesso ou outros desafios que podem afetar a experiência do usuário.
  - Ganhos: nesse caso estamos falando de quaisquer benefícios ou recompensas que o usuário possa experimentar ao utilizar o serviço ou poduto. Isso pode incluir economia de tempo ou facilidade de uso, por exemplo. Que desejos do usuário o serviço ou poduto satisfaz?

## Contexto de uso

- Descreva o ambiente em que o serviço ou poduto deve ser utilizado.
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?

## Jornada do usuário

- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?


<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->
 
## Coleta de dados

## Modelo de tarefas

## Design

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?

### Prototipação em baixo nível (papel)
#### Avaliação heurística

### Prtotipação em médio nível (Figma)
#### Avaliação heurística

### Prtotipação em alto nível (React)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
