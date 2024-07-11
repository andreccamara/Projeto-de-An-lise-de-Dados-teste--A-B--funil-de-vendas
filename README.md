# Projeto final do curso de Análise de Dados da Tripleten -A/B-

# Descrição do Projeto
O projeto é uma tarefa analítica de uma loja online internacional (fictícia). 
O predecessor não conseguiu completá-la: ele lançou um teste A/B e depois desistiu.
Ele deixou apenas as especificações técnicas e resultado dos testes.

O projeto visa trabalhar os dados realizando a análise dos mesmos com foco no resultado do teste A/B

**Descrição técnica**
Nome do teste: recommender_system_test  
Grupos: A (controle) e B (funil de novos pagamentos)  
Data de início: 07-12-2020  
Quando pararam de receber novos usuários: 21-12-2020  
Data de término: 01-01-2021  
Público: 15% de novos usuários da região da UE  
Propósito do teste: testar mudanças relacionadas à introdução de um sistema de recomendação melhorado  
Resultado esperado: em até 14 dias após o cadastro, usuários mostram uma conversão melhor nas visualizações de página do produto (o evento product_page event), em adicionar itens ao carrinho (product_cart) e de compras (purchase). Em cada etapa do funil product_page → product_cart → purchase, haverá ao menos 10% de aumento.  
Número esperado de participantes do teste: 6000

# Objetivos
Identificar a existência estatisticamente relevante de mudanças relacionadas à introdução de uma melhoria do sistema 
Resultado esperado: em até 14 dias após o cadastro, usuários mostrarem uma conversão melhor nas visualizações de página do produto (o evento product_page event), ao adicionar itens ao carrinho (product_cart), e compras (purchase).   

A cada etapa do funil  
**product_page → product_cart → purchase** ,        
terá ao menos 10% de aumento.  

# Ferramentas e Bibliotecas Utilizadas
- Python: Linguagem principal utilizada para a análise.
- Pandas: Biblioteca para manipulação e análise de dados.
- Matplotlib.pyplot, plotly.graph_objects e seaborn: Bibliotecas para criação de gráficos.
- statsmodels.stats.proportion.proportions_ztest: realizar o teste zteste
- scipy.stats.mannwhitneyu: realizar o teste de Mann-Whitney U

# Tabelas:

1. Tabela ab_project_marketing_events_us.csv   
   - o calendário de eventos de marketing para 2020

2. Tabela final_ab_new_users_upd_us.csv   
   - todos os usuários que se cadastraram na loja online de 7 a 21 de dezembro de 2020

3. Tabela final_ab_events_upd_us.csv   
   - todos os eventos dos novos usuários dentro do período de 7 de dezembro de 2020 até 1 de janeiro de 2021

4. Tabela final_ab_participants_upd_us.csv 
   - tabela contendo os participantes do teste

**Estrutura ab_project__marketing_events_us.csv:**
- name — nome dos eventos de marketing
- regions — regiões onde a campanha será realizada
- start_dt — data de início da campanha
- finish_dt — data de término da campanha

**Estrutura final_ab_new_users_upd_us.csv:**
- user_id
- first_date — data de cadastro
- region
- device — dispositivo usado para o cadastro

**Estrutura final_ab_events_upd_us.csv:**
- user_id
- event_dt — data e hora do evento
- event_name — nome da fonte do evento
- details — dados adicionais sobre o evento (por exemplo, o total do pedido em USD para eventos purchase)

**Estrutura final_ab_participants_upd_us.csv:**
- user_id
- ab_test — nome do teste
- group — o grupo de teste ao qual o usuário pertencia

# Metodologia:
- Descrever os objetivos do estudo.
- Importação dos dados
- Explorar os dados:
  - Converter os tipos, se necessário.
  - Verificar a presença de valores ausentes ou duplicados e caracterizá-los, se existirem.
- Realizar a análise exploratória de dados:
  - Estudar a conversão em diferentes etapas do funil.
  - Distribuir igualmente o número de eventos por usuário entre as amostras.
  - Verificar a presença de usuários em ambas as amostras.
  - Analisar a distribuição do número de eventos ao longo dos dias.
  - Considerar quaisquer particularidades nos dados antes de iniciar o teste A/B.
- Avaliar os resultados do teste A/B:
  - Analisar os resultados do teste A/B.
  - Utilizar um z-test para verificar a diferença estatística entre as proporções.
- Descrever as conclusões sobre a etapa da AED e o resultado do teste A/B.

# Resultados
Há diferença estatística entre os grupos, de fato o grupo B apresentou índices de conversões um pouco melhor que o A ~10% melhor e a probabilidade de existir mesmo diferença nas conversões em compras entre os grupos (e não ser apenas uma coincidência) foi consideravelmente alta 98% com zteste e 99% com Mann-Whitney U.

# Aprendizados
Este projeto permitiu-me desenvolver as seguintes habilidades:

- Análise de dados
- Limpeza de dados
- Manipulação de tabelas
- Análise de funil de vendas
- Criação de gráficos interativos.
- Comparação estatística de grupos de teste.
- Realização e avaliação de testes estatísticos Ztest e Mann-Whitney U

# Como Executar o Projeto

- Clone o repositório
- Navegue até o diretório do projeto
- Instale as dependências
- Execute o script principal

## Contato:
Andre Corso Camara
[linkedin](https://www.linkedin.com/in/andre-corso-c%C3%A2mara/)
[email](devandrecorso@hotmail.com)