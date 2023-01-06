# Rede Neural Mamografia
<img src="https://img.shields.io/static/v1?label=Version&message=1.0.0&color=FF2102&style=for-the-badge&logo="/>

Projeto criado visando o funcionamento de uma rede neural que reconhece padrões em uma base de dados e diagnostica mamografias:

 - :white_check_mark: Rede neural:
    - [x] Base de dados;
    - [x] Estrutura;
    - [x] Treinamento;
    - [x] Exportação de pesos;
    - [x] Importação de pesos;
    - [x] Diagnóstico de imagens novas;

---

# Sumário

- [Status](#status)
- [Habilidades desenvolvidas](#habilidades-desenvolvidas)
- [Tecnologias utilizadas](#tecnologias-utilizadas)
- [Organização e Estruturação do Projeto](#organização-e-estruturação-do-projeto)
- [Pré-requisitos](#pré-requisitos)
  - [Ferramentas necessárias](#ferramentas-necessárias)
  - [Executando o projeto](#executando-o-projeto)
  - [Quer contribuir com o projeto?](#quer-contribuir-com-o-projeto)
- [Orientações detalhadas de como utilizar](#orientações-detalhadas-de-como-utilizar)
  - [Setup Inicial](#setup-inicial)
  - [Montar Google Drive](#montar-google-drive)
  - [Verificar conteúdo de imagens](#verificar-conteúdo-de-imagens)
  - [Gerar dataset de treino e validação](#gerar-dataset-de-treino-e-validação)
  - [Visualização de algumas imagens](#visualização-de-algumas-imagens)
  - [Transformações aleatórias da imagem para ampliamento do dataset](#transformações-aleatórias-da-imagem-para-ampliamento-do-dataset)
  - [Otimização do dataset](#otimização-do-dataset)
  - [Construção do modelo](#construção-do-modelo)
  - [Definir ponto de salvamento](#definir-ponto-de-salvamento)
  - [Carregar pesos](#carregar-pesos)
  - [Compilar modelo](#compilar-modelo)
  - [Treinamento por epocas](#treinamento-por-epocas)
  - [Construção de gráfico sobre desempenho em treinamento](#construção-de-gráfico-sobre-desempenho-em-treinamento)
  - [Teste de fotos](#teste-de-fotos)
- [Contribuição](#contribuição)
- [Agradecimentos](#agradecimentos)
- [Autor](#autor)

---

# Status

Este projeto está em desenvolvimento, visando melhoras gráficas e adição de novas funcionalidades.

---

# Habilidades desenvolvidas

- Entender os conceitos básicos de redes neurais;
- Entender os conceitos básicos de base de dados;
- Detectar e solucionar problemas no código de forma mais objetiva;
- Melhorar manutenibilidade e reusabilidade do seu código

---

# Tecnologias utilizadas

- [Google Colab](https://colab.research.google.com/)
- [TensorFlow](https://www.tensorflow.org/)
- [Keras](https://keras.io/)

---

# Organização e Estruturação do Projeto

O projeto está organizado e estruturado da seguinte maneira:
```bash
├── README.md
└── Projeto_Mamografia.ipynb
```

---

# Pré-requisitos

## Ferramentas necessárias

Para rodar o projeto, você vai precisar instalar as seguintes ferramentas:
 - Acesso ao [Google Colab](https://colab.research.google.com/);

## Executando o projeto

 - Faça upload e execute o arquivo Projeto_Mamografia.ipynb no Google Colab
 
 - Tenha um base de dados no [Google Drive](https://drive.google.com/)
  >⚠️ ATENÇÃO ⚠️
  > - Certifique-se que a base de dados esteja no caminho "/content/drive/MyDrive/Projeto/DB";
  > - Certifique-se que divida as classes em subpastas, como "Maligno" e "Saudável";


## Quer contribuir com o projeto?

  - Crie uma branch e faça sua contribuição:

    ```bash
    # Crie uma branch a partir da branch main
    $ git checkout -b nome-da-nova-branch

    # Adicione as mudanças desejadas com os devidos commits
    $ git add . # adiciona as mudanças ao stage do Git
    $ git commit -m 'informação do conteúdo do commit' # salvando as alterações de cada pequena alteração em um commit
    $ git push -u origin nome-da-nova-branch # adiciona a nova branch no repositório remoto do Projeto
    ```
    
  - Crie um novo `Pull Request` (PR):
     - Vá até a página de `Pull Requests` do repositório no GitHub
     - Clique no botão verde `"New pull request"`
     - Clique na caixa de seleção `"Compare"` e escolha a sua branch com atenção
     - Clique no botão verde `"Create pull request"`
     - Adicione uma descrição para o Pull Request
     - Clique no botão verde `"Create pull request"`
     - Me marque para revisar. [Alexandre](https://github.com/AlexandreDinizVeloso)

---

# Orientações detalhadas de como utilizar

## Setup Inicial

 - Descrição: Responsável pela importação de dependências do projeto
     
## Montar Google Drive

- Descrição: Responsável por acessar a base de base de dados do Drive pelo Colab.


## Verificar conteúdo de imagens

- Descrição: Realiza a verificação do conteúdo da pasta, emitindo o nome das subpastas existentes.

## Gerar dataset de treino e validação

- Descrição: Divide as classes da base de dados para treinamento e validação, com proporção padrão de 95% para treinamento e 5% para validação.

## Visualização de algumas imagens

- Descrição: Emite algumas imagens do dataset para verificação.

## Transformações aleatórias da imagem para ampliamento do dataset

- Descrição: Utiliza uma técnica de rotação para ampliar a quantidade de imagens a serem analizadas.

## Otimização do dataset

- Descrição: Utiliza uma técnica de aperfeiçõamento de leitura.

## Construção do modelo

- Descrição: Realiza a construção do modelo da rede neural convolucional.

## Definir ponto de salvamento

- Descrição: Define um local para o armazenamento do peso.

## Carregar pesos

- Descrição: Realiza a importação de um peso, caso possua.

## Compilar modelo

- Descrição: Realiza a preparação do modelo para início do treinamento.

## Treinamento por epocas

- Descrição: Realiza o treinamento da rede neural, por padrão de 100 épocas, com salvamento da melhor época baseado no loss de validação e interrupção do treinamento caso nao tenha sinal de aprimoramento da rede nas últimas 20 épocas.

## Construção de gráfico sobre desempenho em treinamento

- Descrição: Emite um gráfico de desempenho da rede neural no treinamento.

## Teste de fotos

- Descrição: Realiza os testes da rede neural através do upload de uma imagem por url.
  >⚠️ ATENÇÃO ⚠️
  > - Modifique a linha seguinte: urllib.request.urlretrieve("COLOQUE O URL DA MAMOGRAFIA AQUI", "foto.png");

# Contribuição

Bora entrar para esta lista? `;)`

---

# Agradecimentos

Agradeço:
 - À minha família por me apoiar nos estudos;

---

# Autor

 <img src="https://avatars.githubusercontent.com/u/80282868" width="100px;" alt="Minha foto"/>
 <br />
  Alexandre Diniz Veloso
<br />
  Estudante do IFTM.

Entre em contato!

---
