**CICLO DE VIDA DE ENGENHARIA DE USABILIDADE**


1. **Análise das capacidades e restrições da plataforma (Características da Plataforma)**  
   

| Característica | Descrição |
| :---- | :---- |
| Descrição do Software | A camada de software é o núcleo funcional do projeto, composta por uma integração modular de frameworks e ferramentas. Segue uma arquitetura modular e escalável, permitindo a separação entre: camada de visualização (frontend), camada de controle e orquestração (backend) e camada de persistência (bancos de dados). |
| Descrição do Hardware | A plataforma de hardware foi concebida para permitir a execução local de modelos de linguagem de médio porte, com eficiência e baixo custo computacional. Tem como características a compatibilidade com CPU e GPU para inferência local, capacidade de armazenamento suficiente para bancos de dados MongoDB (NoSQL) e Neo4j (grafos) e infraestrutura modular, sem dependência de servidores em nuvem. |
| LISTA DE Capacidades da Plataforma | -> Acessibilidade e Usabilidade - Interface gráfica simples que dispensa conhecimento técnico de programação. <br> -> Execução Local e Autonomia - Utilização do Ollama permite rodar modelos LLM em computadores pessoais, reduzindo custos com nuvem. <br> -> Integração - Capacidade de conectar APIs externas via MCP <br> -> Avaliação Inteligente (LLM-as-a-Judge) - Implementação de um sistema automático de avaliação de desempenho dos fluxos, com feedback textual gerado por um modelo externo.|
| LISTA DE Restrições da Plataforma | -> Limitação de Desempenho - Modelos de menor porte possuem menor capacidade de raciocínio e contexto em comparação com LLMs de grande escala (como GPT-4). <br> -> Escalabilidade Limitada - A arquitetura local não é ideal para fluxos massivos ou simultâneos sem uma camada adicional de distribuição. <br> -> Segurança e Privacidade - Como a execução é local e modular, requer configuração cuidadosa de permissões e autenticações (principalmente no uso de APIs externas via MCP). |

2. **Princípios Gerais do Projeto**     

| Nome | Descrição | Link |
| :---- | :---- | :---- |
| Lei Geral de Proteção de Dados (LGPD) \- Lei n.º 13.709/2018 | A LGPD é a legislação brasileira que regulamenta o tratamento de dados pessoais no Brasil. É importante para o projeto porque estabelece regras sobre como os dados dos usuários devem ser coletados, armazenados, processados e protegidos, garantindo sua privacidade e segurança. | [https://www.planalto.gov.br/ccivil\_03/\_ato2015-2018/2018/lei/l13709.htm](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) |
| ABNT NBR ISO 9241 Ergonomia da interação humano-sistema |  Esta série de normas brasileiras, baseadas nas normas ISO 9241, fornece diretrizes e orientações para o design centrado no usuário de sistemas interativos, incluindo a concepção de interfaces de usuário. A parte 210 aborda o processo de design centrado no humano, enquanto a parte 11 fornece orientações específicas sobre usabilidade. Essas normas são importantes para o projeto porque estabelecem princípios e métodos para garantir que a interface do usuário atenda às necessidades e expectativas dos usuários. | [https://www.inf.ufsc.br/\~edla.ramos/ine5624/\_Walter/Normas/Parte%2011/iso9241-11F2.pdf](https://www.inf.ufsc.br/~edla.ramos/ine5624/_Walter/Normas/Parte%2011/iso9241-11F2.pdf) |

   

3. **Metas de Usabilidade**

   1. **Qualitativo**

    


   2. **Quantitativo**  
    
| Metas | Porcentagem | Justificativa |
| ----- | :---- | :---- |
| Facilidade de … |  |  |
|  |  |  |
|  |  |  |
|  | 1% |  |
|  | 20% |  |
| **Total** | **100%** |  |
