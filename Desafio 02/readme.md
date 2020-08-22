# Desafio 02 | UNINASSAU

- [Desafio 02 | UNINASSAU](#desafio-02--uninassau)
  - [1. Sobre a UNINASSAU](#1-sobre-a-uninassau)
    - [1.1. Introdução](#11-introdução)
  - [2. Desafio de negócio](#2-desafio-de-negócio)
  - [3. Objetivo](#3-objetivo)
  - [4. Desenvolvendo a solução](#4-desenvolvendo-a-solução)
    - [4.1. Pré-requisitos](#41-pré-requisitos)
    - [4.2. Resumo das tarefas](#42-resumo-das-tarefas)
    - [4.3. Desenvolvimento](#43-desenvolvimento)
  - [Resultados](#resultados)

## 1. Sobre a UNINASSAU

### 1.1. Introdução

Fundado em 2003 e com sede no Recife, o Grupo Ser Educacional (B3 SEER3) é um dos maiores grupos privados de educação do Brasil e líder nas regiões Nordeste e Norte em alunos matriculados. A Companhia oferece cursos de graduação, pós-graduação, técnicos e ensino a distância e está presente em 26 estados e no Distrito Federal, em uma base consolidada de aproximadamente 185 mil alunos. A Companhia opera sob as marcas UNINASSAU, UNINASSAU – Centro Universitário Maurício de Nassau, UNINABUCO - Centro Universitário Joaquim Nabuco, Faculdades UNINABUCO, Escolas Técnicas Joaquim Nabuco e Maurício de Nassau, UNIVERITAS/UNG, UNAMA – Universidade da Amazônia e Faculdade da Amazônia e UNIVERITAS – Centro Universitário Universus Veritas, Faculdades UNIVERITAS e a UNINORTE – Centro Universitário do Norte, por meio das quais oferece 1.904 cursos. A UNINASSAU, uma instituição do Grupo Ser Educacional, tem foco na inovação e na trabalhabilidade, oferta aos seus alunos uma formação integral e transformadora. A UNINASSAU prepara profissionais para atuar no ambiente competitivo e dinâmico do mercado de trabalho, empenhados na Responsabilidade Socioambiental, fazendo escolhas, buscando alternativas e valorizando suas competências para criar novas oportunidades. Preocupa-se, acima de tudo, com o ser humano e com sua realização pessoal e profissional.

## 2. Desafio de negócio

O ensino a distância (EaD) proporciona diversas novas possibilidades. Atualmente centenas de estudantes têm acesso aos mesmos conteúdos, participam das mesmas aulas e têm os mesmos professores, tudo de forma remota. Uma das grandes vantagens do EaD é a flexibilidade para que estudantes de todo o país possam trabalhar e estudar ao mesmo tempo. Entretanto, a boa e velha interação interpessoal nem sempre é possível, seja por baixa oferta de horários disponíveis para professores e tutores, ou choques de horários com trabalho e outras obrigações dos estudantes.

Atualmente é possível a realização de uma tutoria remota automática com o auxílio de assistentes virtuais. Esses assistentes podem ser integrados com modelos avançados de aprendizado de máquina, que são alimentados com dados sobre o estudante e seu desempenho nas diferentes disciplinas de seu curso. Esses modelos, por sua vez, podem ser capazes de identificar áreas ou competências específicas em que o estudante tenha certa dificuldade e recomendar conteúdo personalizado para cada aluno, de forma completamente escalável e com atendimento 24/7.

## 3. Objetivo

Neste desafio, o participante irá utilizar ferramentas da IBM como o *Watson Machine Learning* e o *Cloud Pak for Data* para construir um modelo baseado em *machine learning* e integrá-lo com uma solução de assistente virtual, voltada para a tutoria remota. Sua tarefa será aprimorar um modelo já fornecido e integrar os diversos serviços envolvidos nessa solução!

## 4. Desenvolvendo a solução

### 4.1. Pré-requisitos

Para realizar esse desafio você deverá cumprir os seguintes pré-requisitos:

- Possuir uma conta na [IBM Cloud](https://ibm.biz/registro-maratona), podendo ser a conta FREE ou pay-as-you-go (não é necessário registrar-se no evento com o mesmo e-mail utilizado para criar sua conta na IBM Cloud).

### 4.2. Resumo das tarefas

Se você completou o desafio 1, não precisa instanciar novamente o Watson Studio e o Cloud Object Storage (pode usar as mesmas instâncias usadas no desafio anterior).

1. Instanciar o Watson Studio (Cloud Pak for Data as a Service) na IBM Cloud;
2. Instanciar o Watson Machine Learning na IBM Cloud;
3. Instanciar o Cloud Object Storage na IBM Cloud;
4. Importar o projeto fornecido neste repositório [cloud-pak-project-ptbr-2.zip](./cloud-pak-project-ptbr-2.zip) no Watson Studio;
5. Ler e executar as instruções contidas no Notebook ``parte-1.ipynb``;
6. Ler e executar as instruções contidas no Notebook ``parte-2.ipynb``;
7. Acessar a página https://uninassau.maratona.dev, testar e submeter sua solução.

### 4.3. Desenvolvimento

A ideia essencial é criar um modelo baseado em machine learning, capaz de identificar as principais deficiências do aluno, permitindo a realização de uma mentoria estudantil personalizada. Esse é um típico problema de "classificação", onde dadas certas entradas o objetivo do algoritmo é descobrir a "classe" a qual cada estudante pertence.

Por motivos de simplicidade, serão focados em dados de quatro disciplinas do curso de Administração: Matemática Financeira, Empreendedorismo, Direito Empresarial e Gestão Operacional. Utilizando o *Cloud Pak for Data* na IBM Cloud, você irá trabalhar com um conjunto de dados sintético fornecido para criar um modelo capaz de identificar o perfil dos estudantes.

No vídeo abaixo, todo o processo de desenvolvimento da solução é explicado em detalhes. Se você é um iniciante no mundo da ciência de dados e do *machine learning*, é altamente recomendado que você assista ao video para sanar qualquer tipo de dúvida acerca deste desafio.

## Resultados
Os notebooks dá solução se encontram na pasta Desafio-UNINASSAU.
Meu modelo teve 86% de acurácia e recebi a pontuação nesse desafio!