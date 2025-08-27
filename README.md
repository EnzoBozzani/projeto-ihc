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

## Introdução
 
- **Apresente o propósito do produto ou serviço e quais são os principais benefícios que ele oferece aos usuários**: O serviço tem como propósito fornecer uma plataforma para criação de fluxos multi agentes baseados na colaboração entre modelos pequenos. Os fluxos podem ser modelados de maneira que se adequem ao propósito do usuário, que pode depois integrar tais fluxos em seus processos. 
- **Identifique os problemas ou necessidades que o produto ou serviço resolve ou satisfaz**: Hoje, muito se fala da insurgência dos modelos de linguagem e de agentes, mas existem poucas aplicações que abstraem os conceitos técnicos da criação desses agentes, e ainda menos aplicações que fornecem essa abstração por um custo baixo, visto que os LLMs normalmente exigem uma infraestrutura robusta. Por isso, a plataforma preenche esse espaço como centro de criação e aplicação de fluxos baseados em agentes que solucionam problemas complexos de maneira automatizada, eficiente e intuitiva.
- **Liste as características e funcionalidades do seu produto ou serviço de forma detalhada:** A ferramenta tem como funcionalidades principais gerenciamento (criação, visualização e remoção) de fluxos, agentes e recursos (documentos, bancos de dados e e-mail), além da edição de fluxo, onde o usuário conecta os agentes, ferramentas e recursos para montar suas soluções. Os agentes são definidos pela escolha de uma tarefa e modelo, além da possibilidade de acoplar um dos recursos dependendo da tarefa escolhida. As tarefas disponíveis na qual os agentes podem ser especializados são: Orquestração de agentes, Extração de dados de documentos, Acesso a banco de dados, Pesquisa na Internet, Criação de apresentações PowerPoint e Comunicação externa por meio do envio de e-mails. Ao agrupar diferentes agentes em um fluxo, o usuário pode criar as mais diversas automações a serem integradas em sua infraestrutura.
- **Liste as tecnologias e ferramentas computacionais que pretendem usar neste projeto (TCC)**: Python, LangChain, Ollama, Model Context Protocol (MCP), MongoDB, Neo4J, NextJS com TypeScript. 
- **Apresente o contexto de uso dessa aplicação. (“Usuários, tarefas, equipamentos (hardware, software e materiais) e o ambiente físico e social no qual um produto é usado.”)**: Os usuários são, principalmente, empresas que desejam incluir fluxos multi agentes em suas aplicações sem a necessidade de desenvolver código para isso, entretanto qualquer pessoa que busque uma ferramenta para criar fluxos pode usar a aplicação. A aplicação é feita para ser utilizada em qualquer dispositivo que tenha um navegador, podendo ser usada tanto em computadores quanto dispositivos móveis. Como os modelos são hospedados e os fluxos executados em nossa infraestrutura, não há necessidade de hardware potente por parte do usuário para a utilização. O ambiente físico e social é, primariamente, um ambiente corporativo em que os usuários busquem a utilização de múltiplos agentes em seus processos, sem a necessidade de escrever código para criar esses agentes e suas comunicações.

## Publico Alvo

- **Determine qual o grupo específico de pessoas ou organizações para as quais este produto ou serviço é direcionado**: O grupo específico de pessoas ou organizações para as quais o produto é direcionado são empresas e equipes corporativas que desejam incorporar fluxos multiagentes em seus processos de negócio sem a necessidade de desenvolver código. Além disso, embora o foco principal seja o ambiente corporativo, a aplicação também pode atender profissionais individuais, pesquisadores e desenvolvedores não técnicos interessados em criar fluxos de agentes de maneira prática
- **Descreva as caracteristicas demográficas, comportamentais, psicográficas ou geográficas deste público alvo que o torna mais propenso a se interessar pelo que está sendo oferecido neste projeto ou serviço.**
    - **Demografica**: Empresas de médio e pequeno porte e desenvolvedores que dispõem de quantidade limitada de recursos físicos e intelectuais
    - **Comportamentais**: Interesse em fluxo multi agentes para automatização de tarefas; Ferramentas que não necessitam de conhecimentos técnicos profundos
    - **Psicográficas**: Interesse em explorar a inteligência artificial de forma prática e acessível, sem barreiras técnicas de programação.
    - **Geográficas**: Inicialmente mais atrativa em centros urbanos com grande fluxo corporativo, como São Paulo, Rio de Janeiro, Belo Horizonte   

## Análise de concorrência

- **Principais concorrentes ou softwares mais utilizados pelo seu público-alvo:**
   - AutoGPT
   - LangChain
   - AgentVerse
- **Informações sobre os concorrentes selecionados:**

    - AutoGPT destaca-se pela capacidade de automação contínua por meio de agentes autônomos capazes de dividir metas em subtarefas e executá-las com pouca intervenção humana, acessando a internet e armazenando dados. Entretanto, tem limitações significativas, como loops, imprecisões, alto custo e requisitos técnicos.
    - LangChain é um framework modular altamente integrado e versátil, com suporte a workflows complexos, agentes dinâmicos, memória e ampla interconectividade com ferramentas e fontes de dados. Possui soluções complementares como observabilidade (LangSmith) e orquestração avançada (LangGraph), além de forte adoção e comunidade ativa.
    - AgentVerse oferece uma abordagem robusta e estruturada para sistemas multi-agentes, tanto para resolução colaborativa de tarefas quanto para simulações comportamentais. É extensível, performático, escrito em Python, e ideal para estudos de emergências comportamentais em ambientes controlados.

- **Experiência do usuário (UX):**  
<br>
  <img width="500" height="350" alt="AutoGPT" src="https://github.com/user-attachments/assets/f38178dc-5054-44e5-af2e-88e993b895af" />
<br>
    - AutoGPT: Oferece poder de automação impressionante, mas a experiência de uso é pouco intuitiva; exige configuração técnica e acompanhamento para evitar erros.
    - LangChain: Muito flexível e poderoso, mas pensado para desenvolvedores; a experiência é complexa e requer conhecimento técnico, sem foco em usuários leigos.
<br>
  
  <img width="500" height="400" alt="Agentverse" src="https://github.com/user-attachments/assets/81277c6e-c022-4b64-b609-616ba4885380" />
<br>
    - AgentVerse: Voltado para pesquisa e simulação, é robusto, mas a UX ainda é técnica e pouco amigável para usuários não especializados.

- **Modelos de negócio / Preços:**
    - AutoGPT: Open-source, sem modelo de negócio direto; depende da comunidade e do uso das APIs pagas de terceiros (como OpenAI).
    - AgentVerse: Voltado para pesquisa acadêmica, distribuído como open-source; não possui monetização clara, usado principalmente em estudos e experimentos.
    - LangChain: Começou open-source, mas evoluiu para modelo B2B/SaaS, oferecendo ferramentas pagas como LangSmith (monitoramento) e LangGraph (orquestração gerenciada), além de consultoria e suporte corporativo.
    - Todas as 3 plataformas são de uso gratuito, embora possa existir gastos com APIs pagas, infraestrutura, etc.

- **Opiniões de usuários:**
    - AutoGPT e LangChain são muito poderosos, mas difíceis para quem não tem background técnico.
    - Enquanto o AgentVerse é explorado apenas em meio acadêmico, sem foco em usabilidade real.

- **Tendências no mercado:**
    - Hiperautomação com low‑code / no‑code
    - Plataformas low‑code com recursos de IA integrada
    - Evolução para sistemas agentic AI — agentes autônomos e colaborativos
    - Adoção de protocolos padrão para interoperabilidade entre agentes (ex: MCP)
    - Ferramentas e plataformas de IA voltadas para agentes sem necessidade de código para usuários não técnicos

- **Resultados:**
    - O AutoGPT foi pioneiro em automação autônoma, com forte comunidade e versatilidade, mas exige alto conhecimento técnico e apresenta riscos de loops e custos elevados via API.
    - O LangChain consolidou-se como o framework mais robusto, com amplo ecossistema e integrações empresariais, porém é complexo e direcionado a desenvolvedores.
    - O AgentVerse destaca-se em colaboração multiagente e simulações sociais, mas é voltado ao meio acadêmico, com pouca aplicação prática no mercado.
 
    - Enquanto os concorrentes permanecem experimentais, acadêmicos ou excessivamente técnicos, este projeto diferencia-se por oferecer uma plataforma acessível, visual e no-code, com execução local, governança automatizada e templates prontos para aplicações corporativas. Assim, posiciona-se como a solução mais prática para profissionais não técnicos que buscam automatizar fluxos inteligentes sem barreiras.

## Personas

### Persona Primária – Mariana Lopes  

**Status:** Persona Primária  

- **Idade:** 34 anos  
- **Ocupação:** Gerente de Operações em uma empresa de tecnologia financeira (fintech)  
- **Formação:** Administração com MBA em Gestão de Processos  
- **Habilidades:**  
  - Usuária avançada de ferramentas de produtividade (Excel, Power BI, plataformas SaaS).  
  - Não possui conhecimento em programação, mas tem facilidade em aprender ferramentas visuais intuitivas.  

**Tarefas Principais:**  
- Criar fluxos de automação para processos internos (ex: atendimento ao cliente, integração entre sistemas internos e externos).  
- Monitorar métricas de desempenho de processos.  
- Coordenar equipe para que use a plataforma no dia a dia.  

**Objetivos:**  
- Reduzir custos e tempo em tarefas repetitivas.  
- Aumentar a eficiência dos times sem depender de desenvolvedores.  
- Garantir que os fluxos multiagentes sejam configurados de forma clara e reaproveitável.  

**Expectativas:**  
- Que a plataforma seja **no-code**, visual, com interface intuitiva (drag-and-drop).  
- Segurança dos dados corporativos.  
- Documentação simples para rápida adoção pela equipe.  

**Frustrações:**  
- Soluções muito técnicas que exigem programação.  
- Plataformas engessadas que não permitem personalização.  


### Persona Secundária – Rafael Moreira  

**Status:** Persona Secundária  

- **Idade:** 28 anos  
- **Ocupação:** Pesquisador em Inteligência Artificial em uma universidade pública  
- **Formação:** Mestrado em Ciência da Computação (linha de pesquisa: sistemas multiagentes)  
- **Habilidades:**  
  - Familiaridade com conceitos de agentes inteligentes e modelos de IA.  
  - Conhecimento técnico médio (Python, R), mas busca ferramentas que acelerem experimentos.  

**Tarefas Principais:**  
- Criar e testar protótipos de fluxos multiagentes para validar hipóteses acadêmicas.  
- Explorar integrações rápidas sem gastar muito tempo codificando.  
- Publicar resultados de experimentos em artigos e conferências.  

**Objetivos:**  
- Montar rapidamente protótipos para testes de modelos.  
- Comparar diferentes fluxos de agentes em pouco tempo.  
- Ter flexibilidade para adaptar a ferramenta a novos cenários de pesquisa.  

**Expectativas:**  
- Interface flexível, mas sem perder o rigor técnico.  
- Possibilidade de exportar resultados de forma clara (gráficos, logs, relatórios).  
- Colaboração com outros pesquisadores sem barreiras de instalação.  

**Frustrações:**  
- Ferramentas fechadas que não permitem customização.  
- Necessidade de gastar muito tempo configurando ambientes de teste.  

### Persona Negativa – Rafael Lima  

**Status:** Persona Negativa (não público-alvo)  

- **Idade:** 19 anos  
- **Ocupação:** Estudante de curso técnico em outra área (não tecnologia)  
- **Habilidades:** Usa apenas redes sociais, baixo interesse em plataformas acadêmicas.  

**Tarefas:**  
- Não utiliza sistemas de apoio ao aprendizado além do mínimo obrigatório.  

**Objetivos:**  
- Acessar rapidamente uma atividade apenas quando exigido.  

**Expectativas:**  
- Pouco envolvimento.  

**Frustração:**  
- Qualquer plataforma que exija esforço além do básico.  


## Mapa de empatia

### Persona Primária – Mariana Lopes  

<img width="3584" height="2470" alt="persona1" src="https://github.com/user-attachments/assets/12efbdc8-a6a7-40a7-8805-c99369ffd3cc" />

### Persona Secundária – Rafael Moreira 

<img width="3588" height="2470" alt="persona2" src="https://github.com/user-attachments/assets/0735e1d4-063b-47ab-a303-b505f412e9e3" />


## Contexto de uso

- **Descreva o ambiente em que o serviço ou poduto deve ser utilizado**: O webapp será utilizado em ambientes corporativos e profissionais, normalmente em escritórios ou home offices, onde os usuários têm acesso a dispositivos com navegador de internet (computadores, notebooks ou dispositivos móveis). Como os modelos são executados em infraestrutura própria da aplicação, não há necessidade de hardware avançado por parte do usuário. O ambiente, portanto, é digital, conectado à internet e voltado para atividades de gestão e automação de processos empresariais.
- **Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?**
  - Sociais: O uso está inserido em um ambiente de trabalho colaborativo, onde equipes e empresas buscam automatizar tarefas e melhorar a produtividade sem precisar de conhecimento técnico avançado em programação.
  - Econômicos: O foco é em empresas de pequeno e médio porte que precisam de soluções acessíveis, já que grandes LLMs demandam alto custo computacional. A aplicação busca justamente atender esse nicho com modelos menores, mais baratos e eficientes.
  - Culturais: Inserido no contexto atual de adoção crescente de IA e agentes inteligentes, em que existe interesse em experimentar e integrar fluxos multiagentes em diferentes áreas, mas também a necessidade de abstrair a complexidade técnica para que profissionais não técnicos consigam utilizar a ferramenta. 
- **Quais informações sobre o ambiente, o serviço ou produto deve guardar antes de iniciar a interação?** Antes de iniciar a interação, o sistema deve considerar e/ou armazenar informações como:
  - Perfil do usuário (e-mail e senha).
  - Experiência anterior do usuário na plataforma (fluxos, agentes e recursos criados pelo usuário, se existentes).
  - Limites de uso contratados (de acordo com o plano de inscrição do usuário na plataforma).
- **O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou produto?** Quando o usuário acessar a aplicação, normalmente:
  - Ele estará em um ambiente de trabalho (empresa ou home office), provavelmente em horário de expediente.
  - Já estará envolvido em tarefas administrativas, de análise de dados ou automação de processos.
  - O contexto imediato será a necessidade de criar ou editar fluxos de agentes para automatizar tarefas que envolvem documentos, comunicação ou integração com dados.
  - O ambiente digital deverá estar estável: acesso à internet, dispositivo disponível e atenção voltada ao planejamento e execução de processos de negócio.

## Jornada do usuário

Era fim de tarde, e depois de um dia exaustivo de análise de planilhas a fim de identificar movimentos financeiros da empresa em qual trabalha, uma colega comentou sobre uma nova ferramenta que aumentou sua produtividade e diminuiu o cansaço, a partir de fluxos de IA.
Mariana, cansada de realizar tarefas repetitivas e manuais, pensou:
“Será que essa é a solução que tanto procuro?”
Curiosa, acessou o site ainda naquele dia. A proposta era clara: “automatize processos complexos de forma visual.”
Um frio na barriga apareceu: esperança misturada com ansiedade.

Na manhã seguinte, decidiu experimentar.
Criou sua conta em poucos cliques e foi recebida por uma interface interativa: arrastar blocos, conectar linhas e criar fluxos.
Cada passo parecia simples e natural.
Mariana pensava: “É como montar um quebra-cabeça, mas no final quem trabalha é a máquina.”
No mesmo dia, resolveu enfrentar um desafio prático: automatizar o relatório diário de operações.

Então, selecionou a criação de fluxos:
- adicionou um agente que buscava os dados do banco interno;
- conectou a um agente que formatava os números em relatório;
- ligou ao agente de e-mail para enviar automaticamente à diretoria.
Poucos minutos depois, o relatório chegou à sua caixa de entrada.
Ela respirou fundo e pensou: “Consegui! Economizei horas de trabalho com apenas alguns cliques.”
A emoção foi de alívio e orgulho pessoal.

No dia seguinte, em reunião, decidiu mostrar sua conquista.
Os colegas acompanharam atentos, com explicações técnicas mínimas.
Um deles comentou: “Isso resolve em minutos o que levamos horas para fazer.”
Mariana compartilhou o fluxo ali mesmo, em poucos cliques.
Sentiu-se valorizada e confiante, percebendo que tinha dado um passo importante para a modernização da equipe.

Dias depois, entrou no painel de métricas.
Viu que todos os relatórios haviam sido gerados e enviados corretamente, sem erros.
O gráfico mostrava tempo economizado e execuções bem-sucedidas.
Mariana pensou: “Agora posso confiar. Essa plataforma virou meu braço direito.”
A emoção foi de segurança e tranquilidade.


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
