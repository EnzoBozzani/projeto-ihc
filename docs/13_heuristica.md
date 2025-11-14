# Avaliação Heurística 

## Tabela de severidade 
| Grau de Severidade | Tipo           | Descrição                                                   |
|--------------------|----------------|---------------------------------------------------------------|
| 0                  | Sem importância | Não afeta a operação da interface                            |
| 1                  | Cosmético       | Não há necessidade imediata de solução                       |
| 2                  | Simples         | Problema de baixa prioridade (pode ser reparado)             |
| 3                  | Grave           | Problema de alta prioridade (deve ser reparado)              |
| 4                  | Catastrófico    | Muito grave, deve ser reparado de qualquer forma             |


## Criar Agentes
| # | Heurística Violada | Descrição da Violação | Severidade | Imagem |
|---|--------------------|-----------------------|------------|--------|
| 1 | Visibilidade do status do sistema | Ao clicar em “Create”, não há indicador imediato de que o agente está sendo criado. | 2 | <img width="1670" height="918" alt="image" src="https://github.com/user-attachments/assets/62d88820-ef1a-4923-b0c6-e1332ffcbd84" /> |
| 2 | Consistência e padrões | O botão “Create new” nos Agents e Flows muda de posição levemente entre telas. | 1 | <img width="1662" height="918" alt="image" src="https://github.com/user-attachments/assets/522deeea-05bd-4b5e-b082-48b34f866b24" /> |
| 3 | Prevenção de erros | Campos obrigatórios (task/model) não têm destaque visual indicando obrigatoriedade. | 2 | <img width="1673" height="922" alt="image" src="https://github.com/user-attachments/assets/7160d3c9-a671-466f-8f82-78af20be7776" /> |
| 4 | Ajuda e documentação | Falta tooltip explicando o que faz cada “Task” (Orchestrator, SQL Specialist etc.). | 2 |<img width="1673" height="922" alt="image" src="https://github.com/user-attachments/assets/2851773c-a1f9-44e1-98c7-67ad9e3a44f7" /> |

| # | Heurística Violada | Descrição da Violação | Severidade | Imagem |
|---|--------------------|-----------------------|------------|--------|
| 1 | Correspondência com o mundo real | O termo “Model” não é claro para iniciantes; parece nome do agente. | 2 | <img width="1670" height="918" alt="image" src="https://github.com/user-attachments/assets/f4855459-a8f6-4df9-b13f-9961c5793e69" /> |
| 2 | Estética e design minimalista | Menu lateral tem espaçamento excessivo e pouco contraste entre itens. | 1 | <img width="1653" height="917" alt="image" src="https://github.com/user-attachments/assets/586f56ac-dc2a-4a8b-a063-b7e394b5244d" /> | 
| 3 | Reconhecimento ao invés de memorização | Lista de modelos não exibe descrição do modelo (Qwen, Granite etc.). | 2 | <img width="1670" height="918" alt="image" src="https://github.com/user-attachments/assets/67d9cd51-5d1e-4f6c-87f9-ae5fbe25dba3" /> | 
| 4 | Flexibilidade e eficiência de uso | Criar vários agentes exige repetir manualmente passos sem “duplicar agente”. | 1 | <img width="1662" height="918" alt="image" src="https://github.com/user-attachments/assets/24f405c4-0271-4bf1-aed9-23335e885500" /> | 

| # | Heurística Violada | Descrição da Violação | Severidade | Imagem | 
|---|--------------------|-----------------------|------------|--------|
| 1 | Visibilidade do status | Não há feedback claro quando um erro ocorre ao criar agente. | 3 | <img width="1662" height="918" alt="image" src="https://github.com/user-attachments/assets/13e484da-0a30-4d85-8ea8-9ee9369c4d7d" /> |
| 2 | Prevenção de erros | O sistema permite clicar em “Create” com campos vazios antes da validação. | 3 | <img width="1673" height="922" alt="image" src="https://github.com/user-attachments/assets/9e0ccfb1-ed28-45fc-996d-9add6c9d6925" /> |

| # | Heurística Violada | Descrição da Violação | Severidade | Imagem | 
|---|--------------------|-----------------------|------------|--------|
| 1 | Estética e design minimalista | A caixa de seleção de Tasks ocupa muito espaço e não é compacta. | 1 | <img width="1673" height="922" alt="image" src="https://github.com/user-attachments/assets/6ac6944f-5cc2-4a1f-b2c3-06f1a9913c74" /> |
| 2 | Visibilidade | A confirmação “Agent created successfully” aparece discretamente e some rápido. | 2 | <img width="1675" height="923" alt="image" src="https://github.com/user-attachments/assets/a7671be5-e1a0-4b7c-807b-29195df99a4e" /> |
| 3 | Ajuda no diagnóstico de erros | Mensagens de erro não aparecem caso o backend falhe. | 4 | Sem imagem |
| 4 | Reconhecimento | Faltam descrições nos modelos, obrigando o usuário a memorizar o que cada um faz. | 2 | Sem imagem |

----

## Criação de Fluxo

| # | Heurística | Descrição da Violação | Severidade | Imagem |
|---|------------|-----------------------|------------|--------|
| 1 | Visibilidade do status | Ao adicionar agente ao fluxo, não há feedback visível de “ligação criada”. | 2 | <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/74adcdef-d272-4e18-93a4-d188506ac55a" /> | 
| 2 | Prevenção de erros | O usuário pode criar conexões duplicadas sem aviso. | 2 | <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/64680cf4-3158-4a5b-b4e6-1540dcf0808a" /> | 
| 3 | Estética | O fundo pontilhado é pouco contrastante com os nodes e pode confundir. | 1 | <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/42587012-643a-4d13-afe7-a74c9ab21c64" /> |
| 4 | Ajuda e documentação | Não há indicação de como remover um agente do fluxo sem tentar adivinhar. | 2 | Sem imagem | 

| # | Heurística | Descrição da Violação | Severidade | Imagem |
|---|------------|-----------------------|------------|--------|
| 1 | Visibilidade | Não há animação ao conectar agentes, dificultando entender a ação. | 2 |  <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/42587012-643a-4d13-afe7-a74c9ab21c64" /> | 
| 2 | Ajuda | Falta dica explicando por que o orquestrador deve sempre ser o nó central. | 3 |  <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/42587012-643a-4d13-afe7-a74c9ab21c64" /> |

| # | Heurística | Descrição da Violação | Severidade | Imagem |
|---|------------|-----------------------|------------|--------|
| 1 | Visibilidade | Ao arrastar agente, não há guia visual de alinhamento. | 1 |  <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/42587012-643a-4d13-afe7-a74c9ab21c64" /> |
| 2 | Prevenção de erros | O usuário pode criar fluxo sem orquestrador sem receber aviso. | 3 |  <img width="1656" height="917" alt="image" src="https://github.com/user-attachments/assets/732da7cf-9c01-46c1-b582-a4dfaf2c2443" /> |

| # | Heurística | Descrição da Violação | Severidade | Imagem |
|---|------------|-----------------------|------------|--------|
| 1 | Estética | Nodes ficam muito próximos e não existe auto-organização. | 2 |  <img width="1661" height="921" alt="image" src="https://github.com/user-attachments/assets/42587012-643a-4d13-afe7-a74c9ab21c64" />  |

----

##Teste

| # | Heurística | Descrição da Violação | Severidade | Imagem |
|---|------------|-----------------------|------------|--------|
| 1 | Estética | Logs são longos e sem agrupamento. | 2 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/1f03e4ef-7fc3-48e9-8491-687188bd85ff" /> |
| 2 | Diagnóstico de erros | Não há aviso claro quando uma etapa falha. | 3 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/521f85ec-660c-466a-96f7-e2e17f88e05d" /> |

| # | Heurística | Descrição da Violação | Severidade | Imagem |
|---|------------|-----------------------|------------|--------|
| 1 | Prevenção de erros | Botão Enviar não desabilita durante execução. | 3 | <img width="1468" height="814" alt="image" src="https://github.com/user-attachments/assets/451e752b-6a35-4c97-bf6f-cf563e563034" /> |
| 2 | Visibilidade | Resposta final é pouco destacada visualmente. | 2 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/93e43796-8328-4de2-82df-b0bda0a3a7b0" /> |

| # | Heurística | Descrição da Violação | Severidade | Imagens |
|---|------------|-----------------------|------------|---------|
| 1 | Estética | Layout escuro demais, pouco contraste entre Conversa e Logs. | 2 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/bf1ac8d9-da16-431e-810f-c10001dc2de3" /> |
| 2 | Reconhecimento | Timestamps não são claramente separados em coluna. | 1 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/f96a40cc-3f8b-4014-8111-676d9b43239f" /> |
| 3 | Consistência | Estilo das mensagens é muito semelhante (usuário vs sistema). | 2 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/76383441-1545-47b8-9885-95ca77143960" /> |

| # | Heurística | Descrição da Violação | Severidade | Imangens |
|---|------------|-----------------------|------------|----------|
| 1 | Diagnóstico de erros | Interface não mostra mensagens claras de falhas. | 4 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/7e74a67d-a184-460b-9ef2-31b37371cf0f" /> |
| 2 | Flexibilidade | Não é possível clicar nos agentes para ver detalhes da execução. | 2 | <img width="1468" height="814" alt="image" src="https://github.com/user-attachments/assets/5ca52760-2972-4488-a004-4fc2e113a38c" /> |
| 4 | Estética | Logs extensos exigem scroll excessivo. | 2 | <img width="1480" height="811" alt="image" src="https://github.com/user-attachments/assets/3dfabda1-328a-4090-ac3e-aa648347a038" /> |




--------

# Boas Práticas

**Heurística atendida:** Consistência e padrões  
**Descrição:** O sistema mantém um padrão visual consistente para botões de ação ("Create new", "Run flow" e “Enviar”), todos com formato, cor e posição relativamente uniformes. Isso facilita o reconhecimento imediato do objetivo dos botões e reduz a necessidade de aprendizagem adicional.

**Heurística atendida:** Estética e design minimalista  
**Descrição:** A interface utiliza um layout organizado, com elementos bem espaçados e poucos componentes competindo por atenção. O tema escuro com cores suaves para destaques garante leitura confortável e reduz a sobrecarga visual, beneficiando especialmente usuários em telas prolongadas.

**Heurística atendida:** Reconhecimento em vez de memorização  
**Descrição:** Na criação de agentes e fluxos, o usuário recebe listas suspensas com opções visíveis (ex.: Tasks e Models), evitando a necessidade de decorar nomes de modelos ou funções. Essa apresentação direta dos itens reduz erros e agiliza o processo de configuração.

**Heurística atendida:** Controle e liberdade do usuário  
**Descrição:** O sistema permite desfazer ações com facilidade, como remover agentes ou editar fluxos sem necessidade de reiniciar todo o processo. Ícones claros de edição e exclusão oferecem autonomia ao usuário e reforçam a sensação de controle sobre suas configurações.
