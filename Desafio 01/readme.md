# Desafio 01 | Cocamar

- [Desafio 01 | Cocamar](#desafio-01--cocamar)
  - [1. Sobre a Cocamar](#1-sobre-a-cocamar)
  - [2. Desafio de Negócio](#2-desafio-de-negócio)
  - [3. Objetivo](#3-objetivo)
  - [4. Desenvolvendo a Solução](#4-desenvolvendo-a-solução)
    - [4.1 Pré-requisitos](#41-pré-requisitos)
    - [4.2 Resumo das tarefas](#42-resumo-das-tarefas)
    - [4.3 Desenvolvimento](#43-desenvolvimento)
  - [7. Especificações técnicas](#7-especificações-técnicas)
  - [Resultados](#resultados)
  
## 1. Sobre a Cocamar

A Cocamar Cooperativa Agroindustrial foi fundada em 27 de março de 1963, em Maringá (PR). Reuniu, inicialmente, um grupo de 46 fundadores, todos produtores de café. O objetivo era organizar a produção regional, receber e beneficiar o produto. Com o tempo, a cooperativa diversificou os negócios e cresceu. Hoje, a Cocamar está presente em vários municípios por meio de mais de 80 unidades operacionais espalhadas pelo norte e noroeste do Paraná, oeste paulista e sudoeste do Mato Grosso do Sul. Conta com 15 mil associados que atuam com a produção de soja, milho, trigo, café e laranja.

## 2. Desafio de Negócio

O controle de pragas continua sendo um grande desafio para empresas do ramo do agronegócio. Saber identificar rapidamente qual agente está se aproveitando da lavoura é vital para que se possa tomar a ação mais adequada sem comprometer uma grande parte da safra.

As pragas são amplamente conhecidas e, o que falta é um mecanismo rápido de identificação que auxilie o agrônomo na sua tarefa de proteger a lavoura. Sua tarefa é auxiliar na criação dessa ferramenta e aproximar a tecnologia do campo, pois, afinal, agro é tech.

A ideia do desafio é auxiliar o dia a dia do produtor, fornecendo para ele uma ferramenta de reconhecimento visual que o ajude a identificar as pragas.

## 3. Objetivo

O objetivo deste desafio é criar um sistema automático de identificação das pragas que atigem a lavoura de soja citadas acima. Para esse desafio aconselhamos que o participante utilize o _IBM Watson Visual Recognition_ e monte o seu classificador através dele. Antes o participante terá que separar manualmente as imagens da base nas classes citadas anteriormente. Caso considere pertinente, cada participante pode manipular as imagens da base previamente afim de melhorar a acurácia de classificação do modelo do Watson Visual Recognition.

Vamos focar somente nas quatro principais pragas que atigem a lavoura de soja, são elas:

1. Lagarta da soja
2. Percevejo marrom
3. Percevejo pequeno
4. Percevejo verde

*Obs: Os nomes das classes esperadas são apresetados mais abaixo. Não utilize os nomes acima como nome das classes.*

Sua tarefa é buscar imagens dessas pragas e criar um modelo de reconhecimento visual capaz de identificar corretamente cada uma delas, de modo que o agrônomo consiga dar o tratamento adequado.
## 4. Desenvolvendo a Solução

### 4.1 Pré-requisitos

Você deverá cumprir os seguintes itens:
- Registrar na [IBM Cloud](https://ibm.biz/registro-maratona) e confirmar o e-mail de cadastro.

### 4.2 Resumo das tarefas

1. Instanciar o IBM Watson Visual Recognition na IBM Cloud;
2. Instanciar o Watson Studio (Cloud Pak for Data as a Service) na IBM Cloud;
3. Instanciar o Cloud Object Storage na IBM Cloud;
4. Buscar por imagens que representam as classes especificadas: `lagarta`, `percevejo_marrom`, `percevejo_pequeno` e `percevejo_verde`;
5. Treinar o modelo;
6. Subir a aplicação de submissão;
7. Acessar a aplicação de submissão e submeter sua solução.

### 4.3 Desenvolvimento

Nesse repositório, no diretório [dataset](./doc/source/dataset) existem quatro pastas com os nomes das pragas e dentro de cada uma delas há um exemplo de imagem. Use elas como guia para discernir o que é correto dentre as imagens que você encontrar. Além das imagens o diretório também possui um manual de identificação de pragas.
- `lagarta` -> representando a lagarta de soja
- `percevejo_marrom` -> representando o pervejo marrom
- `percevejo_pequeno` -> repressantando o percevejo pequeno
- `percevejo_verde` -> representnado o percevejo verde

## 7. Especificações técnicas

Para a resolução do desafio, você irá utilizar o serviço de [Visual Recognition](https://cloud.ibm.com/catalog/services/visual-recognition) no plano Lite. Nesse plano, existe um limite de 1000 eventos por mês, em que cada evento corresponde, por exemplo, a uma imagem durante o treinamento, ou à classificação de uma imagem. Portanto, tome cuidado ao usar muitas imagens e treinar muitas vezes para não estrapolar o limite do plano, o que invalidaria seu modelo para submissão. Deixe uma margem de pelo menos 100 eventos para que seu modelo possa ser avaliado com sucesso.

_Exemplo: Um usuário estrapola o limite do plano Lite criando 4 classes com 250 imagens cada e treinando o modelo, pois 4 \* 250 = 1000._

## Resultados
A pasta com as imagens é muito grande, por isso não foi adicinada aqui. Foram usadas cerca de 40 imagens para cada classe e 50 para a Classe Negative do Visual Recognition.
Meu modelo Obteve 90% de acurácia nos testes, recebi 4/5 estrelas para esse desafio.