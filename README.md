# Enterprise Operational Intelligence Hub

> Hub de indicadores operacionais para consolidar dados e apoiar decisões de negócio.

**Status:** Planejamento  
**Versão:** 0.1  
**Categoria:** Integração de dados, inteligência operacional e visualização

## 1. Visão geral

O Enterprise Operational Intelligence Hub será uma interface central para consultar indicadores de diferentes áreas de uma empresa fictícia.

O projeto pretende aproveitar um dashboard HTML/CSS já existente, após avaliação de sua estrutura e de como integrá-lo a serviços de dados.

A interface não deverá depender de dados inseridos manualmente no código. Os indicadores serão alimentados por fontes estruturadas e interfaces documentadas.

## 2. Problema de negócio

Indicadores de atendimento, marketing, vendas, finanças e operações podem estar distribuídos em ferramentas diferentes. Isso dificulta construir uma visão consolidada, comparar períodos e identificar gargalos.

## 3. Objetivos

- Consolidar indicadores de diferentes áreas.
- Oferecer uma visão executiva e detalhamento operacional.
- Permitir filtros por período e domínio.
- Automatizar a atualização dos dados.
- Facilitar a identificação de tendências e desvios.
- Integrar progressivamente os outros projetos do portfólio.

## 4. Escopo funcional previsto

### Integração de dados

- Consumir dados de APIs documentadas.
- Normalizar formatos e dimensões necessárias.
- Definir frequência de atualização por fonte.
- Exibir quando os dados foram atualizados.
- Tratar fontes indisponíveis e dados incompletos.

### Indicadores de negócio

- Atendimento: volume, qualidade e resultados de auditoria.
- Marketing e vendas: leads, distribuição e andamento do funil.
- Finanças: conciliação e divergências pendentes.
- Operações: volume processado, tarefas e indicadores específicos.

Os indicadores definitivos dependerão da disponibilidade e da qualidade dos dados de cada projeto.

### Dashboard

- Visão executiva consolidada.
- Páginas ou seções por área.
- Filtros por período e categoria.
- Detalhamento dos indicadores.
- Estados de carregamento, ausência de dados e falha de atualização.
- Identificação da origem e da data de atualização.

## 5. Arquitetura prevista

- **Frontend:** HTML, CSS e JavaScript existentes, adaptados após inspeção.
- **Backend:** Python e APIs, se necessário para consolidação e controle de acesso.
- **Dados:** PostgreSQL ou endpoints específicos dos projetos.
- **Orquestração:** n8n para atualizações e integração.
- **Docker Compose:** execução local.

A escolha definitiva entre consulta direta às APIs e uma camada de consolidação dependerá dos requisitos de atualização, histórico e consistência.

## 6. Princípios de qualidade

- Definir cada indicador, sua fórmula, fonte e periodicidade.
- Não apresentar dados ausentes como zero sem uma regra explícita.
- Diferenciar dados desatualizados de dados atuais.
- Evitar misturar métricas de negócio com métricas de saúde técnica.
- Tratar erros de integração sem ocultar a indisponibilidade da fonte.
- Garantir que os valores exibidos possam ser rastreados até sua origem.

## 7. Testes e critérios de aceitação

A primeira versão deverá demonstrar:

1. Consumo de pelo menos uma fonte estruturada.
2. Exibição de indicadores com fórmulas documentadas.
3. Atualização sem edição manual do frontend.
4. Filtros funcionando corretamente.
5. Tratamento de erros e dados ausentes.
6. Identificação da última atualização.
7. Integração documentada com os serviços utilizados.

## 8. Próximos passos

1. Inspecionar os arquivos do dashboard existente.
2. Inventariar os indicadores desejados.
3. Definir fontes e fórmulas.
4. Projetar contratos de API.
5. Implementar o consumo de dados.
6. Integrar progressivamente os outros projetos.
7. Testar atualização, consistência e apresentação.

## 9. Limitações

O hub não será uma fonte primária de dados financeiros ou operacionais. Ele apresentará indicadores derivados de fontes identificadas, respeitando suas limitações e periodicidade.

## 10. Distinção em relação à Control Tower

Este projeto acompanha o desempenho do negócio. A Automation Control Tower acompanha a saúde técnica, as execuções, os erros e a confiabilidade das automações que alimentam a operação.