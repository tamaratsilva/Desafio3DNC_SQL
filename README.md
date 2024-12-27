# 🚀 Análise de Aquisição de Clientes - Edtech  

Este repositório contém a solução para um desafio analítico voltado ao crescimento de uma empresa Edtech, com foco em aquisição de novos usuários. A proposta envolve a criação de dashboards estratégicos para auxiliar a equipe de negócios no desenvolvimento de ações orientadas por dados.  

## **📋 Contexto**  
Como analista de dados em uma Edtech, fui solicitado a analisar aspectos da aquisição de clientes para avaliar o status do crescimento de novos usuários.  

## **🗂️ Estrutura dos Dados**  

### Tabelas e Campos Disponíveis  
Os dados fornecidos estão organizados em cinco tabelas principais:  

| **Tabela**                      | **Coluna**                             | **Descrição**                                                                                                    |
|---------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `leads_basic_details`           | `lead_id`                              | ID único do lead [string]                                                                                     |
|                                 | `age`                                  | Idade do lead [int]                                                                                           |
|                                 | `gender`                               | Gênero do lead [string]                                                                                       |
|                                 | `current_city`                         | Cidade de residência do lead [string]                                                                         |
|                                 | `current_education`                    | Detalhes da educação atual do lead [string]                                                                   |
|                                 | `parent_occupation`                    | Ocupação do pai do lead [string]                                                                              |
|                                 | `lead_gen_source`                      | Fonte a partir da qual o lead foi gerado [string]                                                             |
| `sales_managers_assigned_leads_details` | `snr_sm_id`                         | ID único do gerente de vendas sênior [string]                                                                 |
|                                 | `jnr_sm_id`                            | ID único do gerente de vendas júnior [string]                                                                 |
|                                 | `assigned_date`                        | Data de atribuição do lead [date]                                                                             |
|                                 | `cycle`                                | Ciclo em que o lead foi atribuído [string]                                                                    |
|                                 | `lead_id`                              | ID único do lead [string]                                                                                     |
| `leads_interaction_details`     | `jnr_sm_id`                            | ID único do gerente de vendas júnior [string]                                                                 |
|                                 | `lead_id`                              | ID único do lead [string]                                                                                     |
|                                 | `lead_stage`                           | Estágio do lead (liderança, conscientização, consideração, conversão) [string]                                |
|                                 | `call_done_date`                       | Data da chamada realizada para o lead [date]                                                                  |
|                                 | `call_status`                          | Status da chamada (successful ou unsuccessful) [string]                                                      |
|                                 | `call_reason`                          | Motivo da chamada, baseado no estágio do lead [string]                                                       |
| `leads_demo_watched_details`    | `lead_id`                              | ID único do lead [string]                                                                                     |
|                                 | `demo_watched_date`                    | Data da sessão de demonstração assistida pelo lead [date]                                                     |
|                                 | `language`                             | Idioma da sessão assistida (Inglês, Telugu, Hindi) [string]                                                   |
|                                 | `watched_percentage`                   | Porcentagem da sessão assistida [float]                                                                       |
| `leads_reasons_for_no_interest` | `lead_id`                              | ID único do lead [string]                                                                                     |
|                                 | `reasons_for_not_interested_in_demo`   | Razão para falta de interesse em assistir à demonstração [string]                                             |
|                                 | `reasons_for_not_interested_in_consideration` | Razão para não considerar o produto [string]                                                                |
|                                 | `reasons_for_not_interested_in_conversion` | Razão para não converter [string]                                                                           |  

---

## **🎯 Objetivo do Desafio**  
O objetivo é criar um dashboard que permita à equipe de negócios desenvolver planos de ação para aumentar o número de usuários cadastrados e impulsionar o crescimento da empresa.  

### **Critérios de Avaliação**  

| **Tipo de Gráfico** | **Descrição**                                                                                                   | **Pontuação** |
|---------------------|---------------------------------------------------------------------------------------------------------------|--------------|
| Pizza               | Quantidade de pessoas masculinas e femininas agrupadas por gênero.                                            | 20           |
| Cartão              | Média de idade dos indivíduos.                                                                                | 20           |
| Barras              | Quantidade de pessoas por tipo de graduação, agrupadas por tipo e ordenadas.                                  | 20           |
| Tabela              | Médias de `watched_percentage` > 0.5, agrupadas por idioma (`language`).                                      | 20           |
| Linhas              | Quantidade de chamadas atendidas por plataformas ao longo do tempo, com todas as linhas no mesmo dashboard.   | 20           |  

---

## **🛠️ Como Começar?**  

1. Acesse a ferramenta Metabase e realize consultas SQL nas tabelas fornecidas:  
   ```sql
   SELECT * FROM leads_basic_details;
   SELECT * FROM sales_managers_assigned_leads_details;
   SELECT * FROM leads_interaction_details;
   SELECT * FROM leads_demo_watched_details;
   SELECT * FROM leads_reasons_for_no_interest;

## Contribuição
Contribuições são bem-vindas! Caso tenha sugestões ou melhorias, sinta-se à vontade para abrir uma issue ou enviar um pull request.

