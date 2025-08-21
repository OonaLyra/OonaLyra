# Documentação do Projeto de Análise de Mercado

## 📌 Visão Geral do Projeto

Este projeto consiste em uma **análise de mercado voltada para prescritores** de produtos/serviços na área de saúde, com foco em nutricionistas e médicos de especialidades relacionadas. O objetivo é entender o perfil, desempenho e engajamento desses profissionais para orientar estratégias comerciais e de relacionamento.

---

## 🎯 Objetivos

- Identificar os prescritores mais ativos e rentáveis.
- Analisar a distribuição geográfica dos prescritores.
- Avaliar a eficácia de diferentes fontes de aquisição.
- Calcular métricas de desempenho como ticket médio, taxa de retenção e tempo de relacionamento.
- Correlacionar participação em eventos com satisfação e desempenho.

---

## 📊 Metodologia

### Fontes de Dados
Os dados foram coletados de um arquivo Excel contendo informações sobre:

- Nome do prescritor
- Especialidade
- Região
- Datas de início e última prescrição
- Receita total e número de prescrições
- Participação em eventos
- Taxa de abertura de cadastro
- Satisfação (escala 1–5)
- Fonte de aquisição

### Ferramentas Utilizadas
- Microsoft Excel para manipulação inicial e fórmulas

---

## 📈 Principais Métricas Calculadas

### 1. Tempo de Relacionamento (meses)
Fórmula:
```excel
=((YEAR(Data Última Prescrição) - YEAR(Data Início)) * 12 + (MONTH(Data Última Prescrição) - MONTH(Data Início)))
```

### 2. Ticket Médio
Fórmula:
```excel
=SE(Número de Prescrições > 0; Receita Total / Número de Prescrições; "0")
```

### 3. Status (Ativo/Inativo)
Critério: prescrição nos últimos 90 dias
```excel
=SE(DIAS(HOJE(); Data Última Prescrição) < 90; "Ativo"; "Inativo")
```

### 4. Taxa de Retenção
```excel
=CONTAR.SE(intervalo_status; "Ativo") / CONTAR(intervalo_status)
```

### 5. Receita por Região
Usando `SOMASE` para agregar receita por região.

---

## 🧠 Análises Realizadas

### Perfil dos Prescritores
- **Especialidades**: Nutricionistas Clínicos, Funcionais, Esportivos; Médicos Gastroenterologistas e Nutrólogos.
- **Regiões**: Todas as cinco regiões do Brasil representadas.
- **Fontes de Aquisição**: Indicação, Instagram, Eventos, Outros.

### Desempenho por Fonte de Aquisição
- Indicações e Instagram são as fontes mais comuns.
- Eventos tendem a atrair prescritores com maior satisfação.

### Correlação entre Variáveis
- Prescritores que participaram de eventos tendem a ter maior satisfação.
- Taxa de abertura de e-mail está parcialmente correlacionada com satisfação.

---

## ✅ Conclusões e Recomendações

### Insights e Recomendações
- Seria eficiente priorizar a reativação dos prescritores com maior taxa de satisfação(5 e 4), do maior tempo de relacionamento para o menor. Estes filtros demonstram a eficiência dos prescritores em manter uma linha com clientes já que mesmo os inativos possuem as quantidades mais altas de prescrições e o ticket médio com maior valor.
- Para realizar a pesquisa de produto e satisfação, eu utilizaria como critérios a taxa de satisfação(5 e 4) e o tempos relacionamento acima de 35 meses, por conta da maior experiência com os produtos e por estes prescritores terem uma alta satisfação entre os clientes.
- A região Norte representa a que menos impacta no total(14,68% do total) bem como tem a menor quantidade de prescritores(48 contra uma média de 60), porém o ticket médio desta região é o terceiro(R$346,63), atrás somente da região Centro-Oeste e Sudeste. Seria eficaz investir em números de prescritores para esta região, caso haja a reativação dos prescritores com maior taxa de satisfação, trazê-los para esta região.
- Indicação e Instagram são Fontes de Aquisição com um ticket médio elevado e uma alta taxa média de abertura mas uma taxa de satisfação menor, seria eficaz investir em priorizar os prescritores destas fontes de aquisição otimizando o onboarding destes e descobrir o que está impactando nessa menor satisfação.
- Nutricionistas Funcionais são 15% dos prescritores totais, mas tem uma receita média 14% maior que a média de todas as especialidades.


---

## 📌 Limitações

- Dados limitados a 300 prescritores.
- Não há informações demográficas adicionais (idade, gênero, etc.).
- Métrica de satisfação subjetiva (escala 1–5).

---

## 👩‍💻 Por Lúcia Katze Lyra
📧 Contato: lu.assis.5bc@gmail.com
📅 Data da última atualização: 22 de agosto de 2025

---

