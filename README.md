# PIB Mensal Brasileiro: Ajuste pela Inflação com IPCA via API do Banco Central

🔄 Este repositório tem como objetivo principal demonstrar o processo de deflação de séries temporais econômicas, convertendo valores nominais em valores reais por meio do Índice de Preços ao Consumidor Amplo (IPCA).

## 📂 Conteúdo
pib_mensal.xls: Base de dados contendo a série histórica do PIB mensal, obtida a partir do IPEAdata.

deflator.ipynb: Notebook em Python que realiza:

- Leitura e pré-processamento da série histórica do PIB;

- Consulta ao IPCA mensal via API SGS do Banco Central do Brasil;

- Cálculo do PIB real (valores deflacionados);

- Visualizações comparativas entre PIB nominal e PIB real.

## 🔗 API Utilizada
Utilizou-se a API de Séries Temporais (SGS) do Banco Central do Brasil para obter os valores mensais do IPCA. O código 433 é empregado para acessar o IPCA amplo consolidado. Os dados são requisitados diretamente via JSON, garantindo atualizações automatizadas e consistência metodológica.

## 📐 Cálculo do PIB Real (Deflacionamento)

O processo de deflação consiste em corrigir os valores nominais do PIB pela inflação, convertendo todos os valores para uma mesma base de comparação.
O resultado representa o valor do PIB a preços constantes, ou seja, com o mesmo poder de compra de junho/2025.

## 📈 Importância da Deflação em Séries Temporais
Trabalhar com valores nominais pode gerar interpretações distorcidas, pois aumentos nos dados podem ser explicados apenas pela inflação. A deflação permite:

- Comparar a evolução real da economia ao longo do tempo;

- Medir o poder de compra real da produção nacional;

- Identificar períodos de crescimento, estagnação ou recessão real;

- Apoiar decisões econômicas e políticas públicas com base em dados consistentes.

## 📊 Análise do Gráfico: PIB Nominal x PIB Real

O gráfico final evidencia a diferença entre os valores nominais (linha azul) e reais (linha verde com marcadores) do PIB mensal:

- A linha azul (PIB nominal) mostra um crescimento acentuado ao longo dos anos, refletindo não apenas a expansão econômica, mas também o efeito cumulativo da inflação.

- A linha verde (PIB real) ajusta esse crescimento ao descontar a inflação, revelando que:

- O crescimento real é mais moderado;

- Há períodos de estagnação ou retração real que não seriam visíveis apenas com os dados nominais;

🔍 O encontro entre as duas curvas no final da série ocorre porque todos os valores foram corrigidos com base no mês de junho de 2025, ou seja, expressos no poder de compra daquele período.

Essa defasagem entre PIB nominal e real é fundamental para compreender o comportamento real da economia e subsidiar decisões fundamentadas em dados consistentes.

