# AGENTS.md — Projeto 2, Sprint 1

## Objetivo
Orientar o desenvolvimento dos códigos Python do Projeto 2 de Estatística e Análise de Dados, seguindo as orientações da Sprint 1 e o material “Explorando a Distribuição Normal — Python”.

## Contexto e escopo
O projeto analisa uma variável quantitativa em duas amostras:
- Planilha 1: dados anteriores à intervenção (espera-se normalmente 300 observações).
- Planilha 2: dados posteriores à intervenção (espera-se normalmente 100 observações).

Não inventar, alterar ou modificar os dados recebidos. Não criar uma variável diferente nem alterar sua unidade de medida. A descrição do problema, a intervenção, os valores de referência e a interpretação final devem ser adaptados ao fenômeno real do grupo.

## Ambiente
- Python no Google Colab.
- Bibliotecas: pandas, numpy, matplotlib, seaborn, scipy e openpyxl.
- Os arquivos de dados devem ser carregados pelo usuário; não incluir dados pessoais ou planilhas privadas no repositório.

## Orientações para o código
1. Carregar as duas planilhas Excel e mostrar nomes de arquivos, colunas e primeiras linhas.
2. Permitir selecionar explicitamente o nome da coluna analisada.
3. Converter a variável para dados numéricos e informar quantos valores válidos restaram após remover valores ausentes/não numéricos.
4. Antes da intervenção, gerar histograma com curva de densidade e boxplot.
5. Calcular média, mediana e desvio-padrão amostral (`ddof=1`).
6. Avaliar a compatibilidade com a normal por:
   - forma do histograma, número de picos e proximidade entre média e mediana;
   - proporções observadas em média ± 1, 2 e 3 desvios-padrão, comparadas à regra empírica aproximada 68%–95%–99,7%;
   - simetria das distâncias entre quartis no boxplot;
   - gráfico Q-Q.
7. Para a Questão 5, calcular `P(a <= X <= b)` pela diferença entre CDFs da normal ajustada com a média e o desvio-padrão amostral, somente quando a aproximação normal for razoável. Os limites `a` e `b` devem vir do contexto real do problema.
8. Para a Questão 6, usar os percentis 20 e 70 da normal ajustada para delimitar, respectivamente, os 20% menores e os 30% maiores valores.
9. Após a intervenção, gerar histograma e boxplot e calcular média, mediana e desvio-padrão amostral.
10. Na Questão 7.4, contar observações da Planilha 2 no intervalo escolhido pelo grupo.
11. Na Questão 8, comparar os cenários com dois critérios relevantes ao objetivo da intervenção, incluindo proporções adequadas ao contexto.
12. Incluir títulos, rótulos dos eixos e unidades de medida em todos os gráficos.
13. Explicar resultados com cuidado: diferenças descritivas entre amostras, isoladamente, não comprovam causalidade nem eficácia estatística da intervenção.

## Qualidade e validação
- Não deixar nomes de colunas, unidades ou limites de exemplo como se fossem dados reais.
- Validar que os dois arquivos e a coluna configurada existem.
- Tratar dados ausentes e valores não numéricos de forma explícita.
- Confirmar que o desvio-padrão é positivo antes de calcular probabilidades ou percentis normais.
- Não concluir que os dados são normais com base em um único gráfico ou critério.
- Manter o código claro, comentado e dividido em células adequadas ao Colab.

## Estrutura sugerida
- `AGENTS.md`: instruções para agentes e colaboradores.
- `README.md`: descrição do projeto e como executar.
- `requirements.txt`: dependências Python.
- `notebooks/`: local para adicionar o notebook do Google Colab exportado pelo grupo.
- `data/`: não versionar planilhas privadas ou dados de participantes.

## Antes de finalizar
Verificar que os limites de intervalo, a unidade de medida, a interpretação dos gráficos e a conclusão estão alinhados à descrição real do fenômeno fornecida ao grupo.
