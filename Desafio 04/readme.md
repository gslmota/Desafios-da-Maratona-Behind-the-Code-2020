# Desafio 04 | Algar
- [Desafio 04 | Algar](#desafio-04--algar)
  - [1. Sobre a Algar](#1-sobre-a-algar)
    - [1.1. Introdução](#11-introdução)
  - [2. Desafio de negócio](#2-desafio-de-negócio)
  - [3. Objetivo](#3-objetivo)
  - [4. Desenvolvendo a solução](#4-desenvolvendo-a-solução)
    - [4.1. Pré-requisitos](#41-pré-requisitos)
    - [4.2. Resumo das tarefas](#42-resumo-das-tarefas)
    - [4.3. Desenvolvimento](#43-desenvolvimento)
  - [Resultados](#resultados)

## 1. Sobre a Algar

### 1.1. Introdução

Há 21 anos repensamos a experiência dos seus clientes e a gestão do ambiente de tecnologia, com um único propósito: conectar pessoas e organizações de um jeito único para ser o melhor parceiro para os seus melhores resultados.

Atuamos em toda a América Latina, e o nosso maior diferencial é a Nossa Gente! Aqui todo mundo se sente em casa. Nosso ambiente é COOL, nossa diversidade é o nosso tempero e o nosso conhecimento é a nossa força.

Nossa missão é conectar pessoas e organizações de um jeito único. Somos feitos para quem busca resultados, e por isso nos comprometemos a transformar o relacionamento entre clientes e empresas por meio de soluções inteligentes.

## 2. Desafio de negócio

O turnover alto gera uma série de custos adicionais, indo muito além do impacto na lucratividade, rentabilidade e o próprio crescimento da organização. A saída em excesso cria um clima inadequado, no qual conflitos interpessoais podem ocorrer com maior frequência, e gerando também a perda de conhecimento. A comunicação interna e externa é afetada, impactando inclusive na atração de novos talentos.

## 3. Objetivo

Este desafio tem como objetivo criar um modelo no *Modeler Flow* (SPSS) capaz de encontrar o melhor candidato de acordo com as variáveis do dataset fornecido. Sua terefa é modelar os dados de tal forma que o modelo que recebe como entrada todas as colunas do dataset e forneça como saída se o candidato deve ser contratado ou não.


## 4. Desenvolvendo a solução

### 4.1. Pré-requisitos

Para realizar esse desafio você deverá cumprir os seguintes pré-requisitos:

- Registrar-se na [Maratona Behind the Code](https://ibm.biz/maratona) e confirmar seu e-mail de cadastro.
- Possuir uma conta na [IBM Cloud](https://ibm.biz/registro-maratona), podendo ser a conta FREE ou pay-as-you-go (não é necessário registrar-se no evento com o mesmo e-mail utilizado para criar sua conta na IBM Cloud).

### 4.2. Resumo das tarefas

1. Instanciar o Watson Studio (Cloud Pak for Data as a Service) na IBM Cloud - ATENÇÃO: Se você já fez o [desafio 2](https://github.com/maratonadev-br/desafio-2-2020) não precisa instanciar um novo, pode usar a mesma;
2. Instanciar o Cloud Object Storage na IBM Cloud - ATENÇÃO: Se você já fez o [desafio 2](https://github.com/maratonadev-br/desafio-2-2020) não precisa instânciar um novo, pode usar a mesma;
3. Criar um projeto em branco no Watson Studio;
4. Clique em 'Add to project' em seguida insira o *Modeler Flow* no projeto;
5. Escolha a opção 'from file' e faça o upload do arquivo [modeler_flow.str](./modeler_flow.str)
6. Adicione os dois arquivos .csv fornecidos neste repositório (pasta data)
7. A saída do seu modelo deve ser uma tabela, você encontra ela no lado esquerdo na aba 'Output'
8. Exporte seu *Modeler Flow* e compacte ele numa pasta zip junto com o arquivo results.csv, conforme mostrado no vídeo abaixo. Você deve submeter ele também
9. Acessar a página [https://algartech.maratona.dev](https://algartech.maratona.dev) e faça upload do arquivo zip com a solução.

### 4.3. Desenvolvimento

A ideia essencial é criar um modelo baseado em machine learning, capaz de contratar o melhor candidato baseado em algumas variáveis permitindo assim a contratação do profissional mais adequado a vaga. Trata-se de um problema de classificação binária, onde a partir da entrada o modelo só existem dois valores possíveis de saída.

Para simplificar o desafio e mostrar ao usuários outras opções de modelagem dentro do Watson Studio (Cloud Pak for Data as a Service) é pedido que seja usado o *Modeler Flow*(SPSS). Sua simplicidade e interface amigável torna acessível o uso, aprendizado e pesquisa na área de ciência de dados por pessoas que não possuem um grande conhecimento em python ou R.

Em linhas gerais, o *Modeler Flow* tem a mesma função de um jupyter notebook, a diferença reside no fato de que a ferramante abstraí a parte do código para focar somente nos dados.

## Resultados
Minhas soluções se encontra na base csv e no arquivo do .str do modeler flow na pasta Algar.
Consegui 4 estrelas nesse desafio.