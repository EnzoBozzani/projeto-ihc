# Cenários de Interação  

## Cenário problema 
Rafael Moreira, pesquisador em IA, desenvolve um estudo em laboratório utilizando bibliotecas de Python, pacotes de machine learning e integração com APIs externas [1]. Seus resultados interessam diretamente ao orientador, colegas de pesquisa e à comunidade científica em conferências [2]. Seu principal objetivo é validar hipóteses sobre a cooperação entre agentes inteligentes, buscando gerar contribuições acadêmicas relevantes [3]. Para isso, Rafael planeja quais arquiteturas utilizar, quais variáveis devem ser controladas e como organizar os fluxos de comunicação [4]. No dia a dia, executa tarefas manuais como programar em Python, ajustar dependências, reconfigurar pacotes e reescrever trechos de código a cada modificação [5]. Ele enfrenta imprevistos como falhas de compatibilidade, instabilidades em APIs externas e prazos apertados de submissão de artigos [6]. Para avaliar seus protótipos, roda simulações, observa logs de interação e verifica se os resultados estão alinhados às hipóteses iniciais [7].

## Cenário Interação  
Rafael Moreira, pesquisador em IA, acessa a plataforma proposta pelo projeto para acelerar o desenvolvimento de seus experimentos. Ao iniciar um novo estudo, o sistema apresenta uma lista de modelos que podem ser especializados em tarefas, cada um associado a uma função específica do processo de pesquisa, como preparação do ambiente, ajuste de dependências, análise de logs e envio de resultados.
Rafael seleciona os modelos que deseja utilizar, indica que tipo de tarefa o agente será especializado e define, de forma interativa, os parâmetros estratégicos para cada um. Após confirmar a configuração, os agentes entram em operação: um agente inicializa automaticamente o ambiente de pesquisa, outro identifica incompatibilidades de pacotes e aplica correções, enquanto um terceiro monitora a execução dos modelos e gera análises interpretativas dos logs. Quando uma inconsistência é detectada, o sistema notifica Rafael e apresenta opções de ajuste com base nos resultados em tempo real. Com o apoio dos agentes, Rafael consegue reduzir significativamente o tempo gasto em tarefas operacionais e direcionar sua atenção para as decisões científicas e validação das hipóteses, garantindo maior eficiência no cumprimento dos prazos de submissão de artigos.

---

## Cenário problema  
Mariana Lopes, gerente de operações em uma fintech, precisa diariamente consolidar dados financeiros vindos de diferentes sistemas internos [1] de maneira precisa e padronizada [3]. Normalmente, exporta planilhas de um banco de dados, copia informações de outro sistema e manualmente organiza relatórios em PowerPoint para apresentar na reunião matinal [4]. A cada atualização, ela gasta horas repetindo processos de copiar e colar, além de conferir se os números estão corretos [5]. Muitas vezes, prazos são comprometidos porque, ao final do dia, Mariana ainda precisa revisar manualmente o conteúdo [6], para verificar se esta correto[7] antes de enviar aos diretores [2]. Esse esforço repetitivo e demorado causa frustração, além de erros humanos frequentes, como informações duplicadas ou dados inconsistentes.

## Cenário interação  

Mariana Lopes, gerente de operações em uma fintech, acessa a plataforma inteligente para consolidar dados financeiros com eficiência. O sistema apresenta uma lista de modelos disponíveis, que podem ser especializados em tarefas específicas como coleta de dados de sistemas internos, validação de consistência, padronização de métricas e geração de relatórios executivos.
Mariana seleciona os modelos e define, de forma interativa, em qual tarefa cada um será especializado e quais parâmetros estratégicos devem ser seguidos (como período de consolidação e nível de detalhamento do relatório). Após a configuração, os agentes entram em operação: um agente se especializa em extrair dados dos sistemas internos, outro valida as informações e detecta duplicidades, enquanto um terceiro gera automaticamente um relatório estruturado no formato exigido pela diretoria.
Se uma inconsistência é encontrada, o sistema notifica Mariana e sugere ações corretivas com base em regras de negócio previamente definidas ou aprendidas. Com esse fluxo, Mariana elimina tarefas repetitivas, reduz erros humanos e consegue focar na interpretação estratégica dos resultados, aumentando a agilidade nas tomadas de decisão e garantindo maior confiabilidade nas informações apresentadas.

---  

## Cenário Problema  
João Henrique, empresário no setor de logística, atua em um ambiente de negociações constantes com transportadoras e fornecedores, onde depende de canais de comunicação como telefone e e-mail [1]. Os atores envolvidos são as equipes de atendimento das empresas parceiras, além dos próprios clientes de João, que aguardam decisões rápidas sobre prazos e custos [2]. Seu principal objetivo é obter informações de forma ágil e confiável para garantir eficiência nos serviços prestados [3]. Para isso, ele planeja contatar os parceiros sempre que surge uma demanda, buscando comparar cotações e alinhar prazos [4]. Na prática, realiza ações repetitivas como ligar diversas vezes, reenviar e-mails e explicar repetidamente sua situação a diferentes atendentes [5]. Eventos externos, como demora na resposta, falhas de comunicação interna nas empresas parceiras ou mudanças repentinas nos prazos de entrega, atrapalham diretamente sua tomada de decisão [6]. Para avaliar se conseguiu sucesso, João verifica a clareza, a rapidez e a consistência das respostas recebidas, além de observar se consegue atender seus próprios clientes sem prejuízos [7].

## Cenário Interação  
João Henrique, empresário do setor de logística, utiliza a plataforma para gerenciar negociações com transportadoras de forma inteligente. Ao iniciar uma nova demanda, o sistema apresenta uma lista de modelos que podem ser especializados em tarefas como negociação automática, análise de risco logístico, comparação de propostas e monitoramento de desempenho.
João seleciona os modelos desejados e define em qual função cada um será especializado, informando variáveis como tipo de carga, rota desejada, prazo máximo e prioridade (custo ou tempo). Assim que confirma a configuração, os agentes entram em operação: um agente inicia contato com transportadoras para coleta de cotações, outro analisa histórico de desempenho e risco, enquanto um terceiro organiza as propostas em um formato comparativo.
Quando uma transportadora apresenta atraso ou dados incompletos, o sistema notifica João e sugere ações, como renegociação automática ou busca de alternativas disponíveis. Com o apoio dos agentes especializados, João não precisa mais realizar ligações manuais ou repetir solicitações, e passa a atuar diretamente como decisor estratégico, garantindo rapidez e eficiência nas operações logísticas.  


# Diagrama de Falas

| **Tópico > Subtópico**     | **Falas e signos**                                                                                |
|---------------------------|----------------------------------------------------------------------------------------------------|
| **Criar fluxo**           | U: Preciso criar um **fluxo** utilizando múltiplos **agentes**                                     |
| **> Informar modelos**    | D: Quantos **modelos** você deseja utilizar?                                                       |
|                           | U: Quero 4 modelos                                                                                 |    
| **> Especializar modelos**| D: Quais **tarefas** os modelos devem executar?                                                    |
|                           | U: Preparar **ambiente**, ajustar **dependências**, analisar **logs** e enviar **resultados**      |
|                           | D: Deseja nomear os agentes?                                                                       |
|                           | U: Sim, os nomes serão X, Y, Z                                                                     |
| **> Execução do fluxo**   | U: Execute o fluxo                                                                                 |
|                           | D: Fluxo iniciado. Monitorando agentes...                                                          |
| **> Envio de resultados** | U: Enviar o **relatório** final aos **destinatários**                                              |
|                           | **D:** Resultado enviado com sucesso                                                               |              


| **Tópico > Subtópico**        | **Falas e signos**                                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Criar fluxo financeiro**   | U: Preciso consolidar os dados financeiros utilizando múltiplos agentes **especializados**                                    |
| **> Informar modelos**       | D: Quantos modelos/agentes você deseja utilizar no fluxo de consolidação?                                                     |
|                              | U: Quero 3 agentes                                                                                                            |
| **> Especializar modelos**   | D: Quais **funções** cada agente deve executar?                                                                               |
|                              | U: Um deve coletar os dados dos **sistemas internos**, outro validar **inconsistências** e o terceiro gerar o relatório final | 
|                              | D: Deseja nomear os agentes?                                                                                                  |
|                              | U: Sim, Coleta_AI, Valida_AI e Relatorio_AI                                                                                   | 
| **> Execução do fluxo**      | U: Execute o fluxo de consolidação                                                                                            |
|                              | D: Iniciando coleta de dados. Um alerta: dados duplicados foram detectados. Deseja aplicar correção automática?               | 
|                              | U: Sim, aplicar correção                                                                                                      |
| **> Geração de relatório**   | U: Gerar versão **executiva** para **apresentação**                                                                           |
|                              | D: Relatório gerado com **indicadores** consolidados. Deseja exportar para **PDF** ou enviar diretamente aos **diretores**?   |
|                              | U: Enviar aos diretores                                                                                                       |
| **> Finalização**            | D: Resultado enviado com sucesso. Deseja salvar este fluxo para uso diário **automático**?                                    |



| **Tópico > Subtópico**       | **Falas e signos**                                                                                                 |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Criar fluxo logístico**   | U: Preciso iniciar uma negociação logística com múltiplos agentes especializados                                    |
| **> Informar modelos**      | D: Quantos modelos/agentes você deseja utilizar na negociação?                                                      |
|                             | U: Quero 3 agentes                                                                                                  |
| **> Especializar modelos**  | D: Quais funções cada agente deve executar?                                                                         |
|                             | U: Um deve buscar **cotações**, outro avaliar **risco logístico** e o terceiro analisar **custo-benefício**         |
|                             | D: Deseja nomear os agentes?                                                                                        |
|                             | U: Sim, Cotacao_AI, Risco_AI e Decisao_AI                                                                           |    
| **> Execução do fluxo**     | U: Inicie a negociação com os fornecedores cadastrados                                                              |
|                             | D: Fluxo iniciado. Cotacao_AI está coletando propostas. Risco_AI está avaliando **desempenho** histórico.           |
|                             | D: Uma transportadora atrasou na **resposta**. Deseja reenviar solicitação automaticamente?                         |  
|                             | U: Sim, reenviar                                                                                                    |
| **> Análise dos resultados**| U: Exiba a melhor proposta com base no equilíbrio entre custo e prazo                                               |
|                             | D: A melhor opção encontrada é da transportadora Z. Prazo dentro do limite e risco considerado baixo.               |
| **> Decisão final**         | U: Confirmar contratação da transportadora Z                                                                        |
|                             | D: Contratação registrada com sucesso. Deseja salvar este fluxo para futuras negociações automáticas?               |
