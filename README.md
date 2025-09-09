# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel).

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **PESQUISA E IMPLEMENTAÇÃO DE PLATAFORMA PARA CRIAÇÃO DE FLUXOS MULTI-AGENT** sob orientação do Professor **Prof. Dr. Flavio Tonidandel** e desenvolvido pelos seguintes alunos:

-   Adriel Henrique Foppa Lima - 22.225.036-7
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

## Conhecendo o problema

-   **Apresente o propósito do produto ou serviço e quais são os principais benefícios que ele oferece aos usuários**: O serviço tem como propósito fornecer uma plataforma para criação de fluxos multi agentes baseados na colaboração entre modelos pequenos. Os fluxos podem ser modelados de maneira que se adequem ao propósito do usuário, que pode depois integrar tais fluxos em seus processos.
-   **Identifique os problemas ou necessidades que o produto ou serviço resolve ou satisfaz**: Hoje, muito se fala da insurgência dos modelos de linguagem e de agentes, mas existem poucas aplicações que abstraem os conceitos técnicos da criação desses agentes, e ainda menos aplicações que fornecem essa abstração por um custo baixo, visto que os LLMs normalmente exigem uma infraestrutura robusta. Por isso, a plataforma preenche esse espaço como centro de criação e aplicação de fluxos baseados em agentes que solucionam problemas complexos de maneira automatizada, eficiente e intuitiva.
-   **Liste as características e funcionalidades do seu produto ou serviço de forma detalhada:** A ferramenta tem como funcionalidades principais gerenciamento (criação, visualização e remoção) de fluxos, agentes e recursos (documentos, bancos de dados e e-mail), além da edição de fluxo, onde o usuário conecta os agentes, ferramentas e recursos para montar suas soluções. Os agentes são definidos pela escolha de uma tarefa e modelo, além da possibilidade de acoplar um dos recursos dependendo da tarefa escolhida. As tarefas disponíveis na qual os agentes podem ser especializados são: Orquestração de agentes, Extração de dados de documentos, Acesso a banco de dados, Pesquisa na Internet, Criação de apresentações PowerPoint e Comunicação externa por meio do envio de e-mails. Ao agrupar diferentes agentes em um fluxo, o usuário pode criar as mais diversas automações a serem integradas em sua infraestrutura.
-   **Liste as tecnologias e ferramentas computacionais que pretendem usar neste projeto (TCC)**: Python, LangChain, Ollama, Model Context Protocol (MCP), MongoDB, Neo4J, NextJS com TypeScript.
-   **Apresente o contexto de uso dessa aplicação. (“Usuários, tarefas, equipamentos (hardware, software e materiais) e o ambiente físico e social no qual um produto é usado.”)**: Os usuários são, principalmente, empresas que desejam incluir fluxos multi agentes em suas aplicações sem a necessidade de desenvolver código para isso, entretanto qualquer pessoa que busque uma ferramenta para criar fluxos pode usar a aplicação. A aplicação é feita para ser utilizada em qualquer dispositivo que tenha um navegador, podendo ser usada tanto em computadores quanto dispositivos móveis. Como os modelos são hospedados e os fluxos executados em nossa infraestrutura, não há necessidade de hardware potente por parte do usuário para a utilização. O ambiente físico e social é, primariamente, um ambiente corporativo em que os usuários busquem a utilização de múltiplos agentes em seus processos, sem a necessidade de escrever código para criar esses agentes e suas comunicações.

## Publico Alvo

-   **Determine qual o grupo específico de pessoas ou organizações para as quais este produto ou serviço é direcionado**: O grupo específico de pessoas ou organizações para as quais o produto é direcionado são empresas e equipes corporativas que desejam incorporar fluxos multiagentes em seus processos de negócio sem a necessidade de desenvolver código. Além disso, embora o foco principal seja o ambiente corporativo, a aplicação também pode atender profissionais individuais, pesquisadores e desenvolvedores não técnicos interessados em criar fluxos de agentes de maneira prática
-   **Descreva as caracteristicas demográficas, comportamentais, psicográficas ou geográficas deste público alvo que o torna mais propenso a se interessar pelo que está sendo oferecido neste projeto ou serviço.**
    -   **Demografica**: Empresas de médio e pequeno porte e desenvolvedores que dispõem de quantidade limitada de recursos físicos e intelectuais
    -   **Comportamentais**: Interesse em fluxo multi agentes para automatização de tarefas; Ferramentas que não necessitam de conhecimentos técnicos profundos
    -   **Psicográficas**: Interesse em explorar a inteligência artificial de forma prática e acessível, sem barreiras técnicas de programação.
    -   **Geográficas**: Inicialmente mais atrativa em centros urbanos com grande fluxo corporativo, como São Paulo, Rio de Janeiro, Belo Horizonte

## Desenvolvimento

-   [Análise de Concorência](docs/2_concorencia.md)
-   [Personas](docs/3_personas.md)
-   [Cenário de Análise/Problema](docs/4_cenarios.md)
-   [Análide de Tarefas](docs/5_analise_tarefas.md)
-   [Prototipação em Papel](docs/6_prototipacao.md)
-   [Coleta de Dados](docs/7_coleta_dados.md)
-   [Ciclo de vida da engenharia de usabilidade](docs/8_ciclo_vida.md)
-   [Modelo Conceitual](docs/9_modelo_conceitual.md)
-   [MOLIC](docs/10_molic.md)
-   [FIGMA](docs/11_figma.md)
-   [Planejamento da Avaliação](docs/12_planejamento_avaliacao.md)
-   [Avaliação de IHC através de Inspeção Heurística](docs/13_heuristica.md)
-   [Avaliação de Usabilidade baseado em Observação do Usuário](docs/14_observacao_usuario.md)
