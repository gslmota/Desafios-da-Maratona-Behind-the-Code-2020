# Desafio 06 | LIT
- [Desafio 06 | LIT](#desafio-06--lit)
  - [1. Sobre a LIT](#1-sobre-a-lit)
  - [2. Desafio de negócio](#2-desafio-de-negócio)
  - [3. Objetivo](#3-objetivo)
  - [4. Desenvolvendo a solução](#4-desenvolvendo-a-solução)
    - [4.1. Pré-requisitos](#41-pré-requisitos)
    - [4.2. Resumo das tarefas](#42-resumo-das-tarefas)
    - [4.3. Desenvolvimento](#43-desenvolvimento)
  - [Resultados](#resultados)

## 1. Sobre a LIT

O LIT é a plataforma digital de cursos da Saint Paul Escola de Negócios, eleita por cinco vezes uma das melhores escolas de negócios do mundo, segundo a Financial Times. 

É uma plataforma de cursos de educação executiva que conta com desde conteúdos tradicionais a  inovadores de negócios. Baseado na metodologia de aprendizagem Onlearning, em micro-momentos, micro-certificações e aprendizagem em rede, o aluno do LIT, por um valor único mensal, tem acesso ilimitado a mais de 150 cursos de diversas áreas e dificuldades.

## 2. Desafio de negócio

O LIT faz personalização do ensino com o "Paul", o primeiro tutor do mundo a utilizar a tecnologia de Inteligência Artificial IBM Watson para potencializar a aprendizagem e também a personalização, visando  ajudar o aluno a estudar da forma mais adequada para absorver o máximo de conteúdo possível sem desfocar do que ele realmente deve aprender, eliminando assim conteúdos que o aluno já sabe.
 
Nesse Desafio de Segmentação de Mercado, os participantes deverão dividir por segmentos comportamentais e por competências os alunos do LIT, para gerar uma experiência na plataforma ainda mais personalizada. 

Para tanto, neste desafio deverá ser desenvolvido uma solução tecnológica para segmentar os alunos por comportamento e competências.
 
Do ponto de vista comportamental, os alunos deverão ser divididos em 6 grupos a partir da interação do aluno ao longo de sua jornada no LIT. Cada perfil busca medir o grau de esforço do aluno dentro do progama educacional e qual a melhor jornada para o estudante.
 
Com a introdução de um novo processo de onboarding na plataforma, teemos a oportunidade de utilizar os dados preenchidos pelos alunos para fazer uma melhor recomendação de quais dos mais 150 cursos do LIT, o aluno deveria se matricular, focando em seus interesses e responsabilidades.
 
Sendo assim, esperamos poder indicar para cada aluno do LIT quais são os cursos ideais para ele, de acordo com as competências que eles precisam desenvolver para a sua carreira. Esperamos também durante a sua jornada de aprendizagem no LIT, gerar ações de engajamento de acordo com sua atividade na plataforma. 


## 3. Objetivo

Neste desafio, você deverá utilizar um jupyter notebook para criar um modelo de aprendizado de máquina capaz, com base nas variáveis fornecidas no dataset, identificar o que define o perfil de cada aluno para poder realizar previsões sobre futuros alunos.

## 4. Desenvolvendo a solução

### 4.1. Pré-requisitos

Para realizar esse desafio você deverá cumprir os seguintes pré-requisitos:

- Registrar-se na [Maratona Behind the Code](https://ibm.biz/maratona) e confirmar seu e-mail de cadastro.
- Possuir uma conta na [IBM Cloud](https://ibm.biz/registro-maratona), podendo ser a conta FREE ou pay-as-you-go (não é necessário registrar-se no evento com o mesmo e-mail utilizado para criar sua conta na IBM Cloud).

### 4.2. Resumo das tarefas

1. Iniciar o `notebook.ipynb` e seguir todas as instruções
2. Compactar o arquivo `results.csv` e `notebook.ipynb` em arquivo zip (pode usar qualquer nome).
3. Acessar [https://lit.maratona.dev/](https://lit.maratona.dev/) e realizar sua submissão.

### 4.3. Desenvolvimento

O objetivo principal desse desafio é criar um modelo baseado em machine learning, capaz de identificar o perfil de cada aluno, permitindo a realização de uma jornada estudantil personalizada. Esse é um típico problema de "classificação", onde dadas certas entradas o objetivo do algoritmo é descobrir a "classe" a qual cada estudante pertence.

Foram definidos seis tipo de perfis, cada um medindo o grau de esforço do aluno durante sua jornada no LIT. Sua tarefa é criar um modelo capaz de entender como os perfis se comportam para poder prever qual o perfil de futuros alunos do LIT, personalizando assim a jornada do estudante.

Para esse desafio você vai utlizar um jupyter notebook para criar o seu modelo utilizando como base o dataset `training_dataset.csv`. Fique a vontade para criar novas variáveis e novas colunas no dataset fornecido, pois, diferentemente dos desafios anteriores, neste desafio não será necessário nesse desafio fazer o deploy da solução no Watson MAchine Learning, contudo, você deverá preencher os perfis da planilha `results.csv` utilizando o seu modelo.

Com o aquivo `results.csv` devidamente preendchido voce deve compactá-lo junto com o seu notebook da seguinte forma e com os respectivos nomes:
```bash
meu_zip.zip
|-results.csv
|-notebook.ipynb
```
## Resultados
Os arquivos da minha solução se encontram na pasta Lit.
Nesse desafio obtive 5 estrelas.