# Desafio 07 | TNT
- [Desafio 07 | TNT](#desafio-07--tnt)
  - [1. Sobre a TNT](#1-sobre-a-tnt)
    - [1.1. Introdução](#11-introdução)
  - [2. Desafio de negócio](#2-desafio-de-negócio)
  - [3. Objetivo](#3-objetivo)
  - [4. Desenvolvendo a solução](#4-desenvolvendo-a-solução)
    - [4.2. Pré-requisitos](#42-pré-requisitos)
    - [4.3. Resumo das tarefas](#43-resumo-das-tarefas)
    - [4.4. Desenvolvimento](#44-desenvolvimento)
  - [Resultados](#resultados)

## 1. Sobre a TNT

### 1.1. Introdução

A marca TNT está presente em 20 estados brasileiros, principalmente nas regiões Sul e Sudeste. Produzido em Teresópolis/RJ, está entre os três energéticos mais consumidos no Brasil e é comercializado nas seguintes versões: Original, Açaí com Guaraná, Citrus, Pêssego, Maçã Verde, Tangerina e Zero Açúcar. Pioneiro, foi o primeiro energético brasileiro a utilizar o selo higiênico e permanece o único.
## 2. Desafio de negócio

O mercado de energéticos vem crescendo ano após ano, muito impulsionado por mudanças no hábito de consumo do brasileiro, o que antigamente era um produto apenas de mixologia, passou a ser um produto de consumo diário por conta das suas funcionalidades.

Com esse crescimento e novos hábitos de consumo, os pontos de vendas ganharam uma atenção ainda maior, uma vez que, os produtos precisam estar à disposição do cliente nos momentos que eles necessitam dessas funcionalidades.

Negociações comerciais com grandes redes de varejo necessitam de muitos esforços de investimentos e nem sempre é o momento que o cliente mais necessita do produto.
Como desafio, TNT Energy Drink quer propor uma opção de utilização das vending machines como PDV nos momentos que os clientes mais necessitam (Metrôs, Academias etc.).

Cada vending machine servirá como um grande banco de dados fornecendo informações em tempo real de quantidade de produtos, possibilitando o melhor controle de estoque, recomendação de reabastecimentos, melhores pontos de vendas, etc. 

## 3. Objetivo

Os desenvolvedores deverão utilizar IBM Watson Studio, e IoT na IBM Cloud para criar um modelo preditivo capaz de alertar momento ideal que será necessária uma nova recarga de uma máquina de venda automática de TNT. Os participantes deverão se conectar a dispositivos IoT para receber os dados de estoque das máquinas em tempo real, e ajudar a empresa na reposição, onde a máquina de venda automática somente será visitada quando houver a necessidade de reabastecimento, poupando gastos desnecessários.

## 4. Desenvolvendo a solução

### 4.2. Pré-requisitos

Para realizar esse desafio você deverá cumprir os seguintes pré-requisitos:

- Registrar-se na [Maratona Behind the Code](https://ibm.biz/maratona) e confirmar seu e-mail de cadastro.
- Possuir uma conta na [IBM Cloud](https://ibm.biz/registro-maratona), podendo ser a conta FREE ou pay-as-you-go (não é necessário registrar-se no evento com o mesmo e-mail utilizado para criar sua conta na IBM Cloud).

### 4.3. Resumo das tarefas

1. Se conectar ao broker IoT e adquirir os dados de consumo e abastecimento dos pontos de venda
2. Formatar os dados em um aquivo csv
3. Importar os dados em [notebook.ipynb](./notebook.ipynb) e modelar
4. Compactar o arquivo `results.csv` e `notebook.ipynb` em arquivo zip (pode usar qualquer nome).
5. Acessar [https://tnt.maratona.dev/](https://tnt.maratona.dev/) e realizar sua submissão.

### 4.4. Desenvolvimento

O desafio será dividido em duas partes. A primeira parte se refere a aquisição dos dados. A segunda é relativo a modelagem dos dados adquiridos na etapa anterior.

A TNT, em conjunto com a organização da Maratona criou um dispotivo IoT que está publicando dados referentes ao seus postos de venda num tópico. Os dados publicados pelo dispotivo IoT formaram a base necessária para construir a segunda parte do desafios. O Dispotivo ficará ligado até o fim da Maratona e basta apenas uma hora para você adiqurir todos os dados. Junto dos dados vai vir um indice para saibam quando a base começar a se repetir.

Para adiquirir os dados será necessário se conectar ao seguinte endereço por meio do protocolo `MQTT` com a seguinte configuração:

```bash
HOST: tnt-iot.maratona.dev
PORT: 30573
USERNAME: maratoners
PASSWORD: ndsjknvkdnvjsbvj
```

Para adquirir os dados é necessário "ouvir" o tópico `tnt`, e eles vão vir no seguinte formato.

```josn
{
  "row": 2000,
  "Tempo": "aaaa-mm-dd",
  "Estação": "metro",
  "LAT": "Latitude",
  "LONG": "Longitude",
  "Movimentação": 123123,
  "Original_473": 100,
  "Original_269": 100,
  "Zero": 100,
  "Maçã-Verde": 100,
  "Tangerina": 100,
  "Citrus": 100,
  "Açaí-Guaraná": 100,
  "Pêssego": 100,
  "TARGET": "status"
}
```

Um vez de posse de todos os dados você deverá formatar eles num arquivo csv de modo que a primeira linha seja cobeçalho do aquivo e o restante somente com os dados adquiridos pelo dispositivo IoT, como mostra o formato abaixo.

```csv
Tempo,Estação,LAT,LONG,Movimentação,Original_473,Original_269,Zero,Maçã-Verde,Tangerina,Citrus,Açaí-Guaraná,Pêssego,TARGET
2010-1-1,Corinthians-Itaquera,-21.0163,-48.7739,70277,86,65,65,43,43,43,43,43,NORMAL
2010-1-1,Palmeiras-Barra Funda,-21.0163,-48.7800,70376,86,65,65,43,43,43,43,43,NORMAL
...
```

Com os dados formatados em csv, chegou a hora de criar um modelo de aprendizado de máquina capaz de identificar a partir de qual quantidade de produtos no ponto de vendas é necessário reabastecimento. Para isso, foi fornecido o notebook [notebook.ipynb](./notebook.ipynb) contendo as intruções necessária a modelagem. Fique a vontade para criar novas variáveis e colunas no dataset obtido, pois, semelhante ao [desafio 6](https://github.com/maratonadev-br/desafio-6-2020), neste desafio não será necessário fazer o deploy da solução no Watson Machine Learning, contudo, você deverá preencher a coluna `TARGET` da planilha results.csv utilizando o seu modelo.

Com o aquivo results.csv devidamente preendchido voce deve compactá-lo junto com o seu notebook da seguinte forma e com os respectivos nomes:

```bash
meu_zip.zip
|-results.csv
|-notebook.ipynb
```
## Resultados
Minha solução se encontra na pasta TNT, além disso tem o data_set coletado usando o Node Red.
Obtive 5 estrelas nesse desafio.
