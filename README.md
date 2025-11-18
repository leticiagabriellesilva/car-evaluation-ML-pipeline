# 🚗 Projeto de Esteira de Machine Learning: Avaliação de Carros
### 📝 Descrição do Projeto
Este repositório contém um pipeline completo de Machine Learning (ML) implementado em um notebook Python (```.ipynb```), utilizando a base de dados "Car Evaluation Database" (Avaliação de Carros).

O objetivo é treinar um modelo de Árvore de Decisão para classificar a aceitabilidade de um carro (classes: ```unacc```, ```acc```, ```good```, ```vgood```) com base em seis atributos de entrada (preço de compra, manutenção, portas, capacidade de pessoas, tamanho do porta-malas e segurança).

#### A esteira de ML inclui as etapas de:

1. Carregamento de Dados (diretamente do Google Drive).

2. Pré-processamento (Transformação de variáveis categóricas em numéricas, conhecido como Ordinal Encoding).

3. Divisão de Dados em conjuntos de Treinamento, Validação e Teste.

4. Treinamento do Modelo (DecisionTreeClassifier).

5. Avaliação (Acurácia e Matriz de Confusão).

6. Simulação de Predição ("Implantação").

### 🛠️ Tecnologias Utilizadas

- Linguagem: Python
- Ambiente de Execução: Google Colab
- Bibliotecas:
  - ```pandas``` (Manipulação de dados)
  - ```numpy``` (Cálculos numéricos)
  - ```scikit-learn``` (Modelagem de Machine Learning)
  - ```matplotlib``` & ```seaborn``` (Visualização de dados)
 
### 🚀 Como Reproduzir a Execução
Siga os passos abaixo para executar o notebook no seu ambiente:

#### Passo 1: Preparação dos Dados no Google Drive

1. Faça o upload do arquivo de dados ```car.data``` para o seu Google Drive.

2. Anote o caminho: Por padrão, o caminho será ```/content/drive/MyDrive/car.data```. Se você colocou em uma subpasta (ex: ```ML_Projetos```), o caminho será ```/content/drive/MyDrive/ML_Projetos/car.data```.

#### Passo 2: Configuração e Execução no Google Colab

1. Abra o Google Colab e crie um Novo notebook (```.ipynb```).

2. Copie o código fornecido (Células 3, 5, 7 e 9) para as células de ```+ Código``` do seu notebook.

3. Célula de Conexão (Célula 3):

  - Execute a primeira célula que contém o comando ```drive.mount('/content/drive')```.

  - Um pop-up pedirá autorização. Clique em *"Conectar ao Google Drive"* e conceda as permissões necessárias.

  - Ajuste o Caminho: Edite a variável ```caminho_arquivo``` na Célula 3 para refletir o local exato do seu arquivo ```car.data``` no Google Drive.

```dash
# Exemplo de ajuste:
# caminho_arquivo = '/content/drive/MyDrive/car.data' 
# OU
# caminho_arquivo = '/content/drive/MyDrive/SuaPasta/car.data'
```

#### Passo 3: Execução Sequencial da Esteira

Execute as células de código uma por uma, de cima para baixo. Use o atalho ```Shift + Enter``` ou clique no ícone ▶ (Play) ao lado de cada célula.

| Célula | Objetivo                                                       | Verificação                                               |
|--------|----------------------------------------------------------------|-----------------------------------------------------------|
| 3      | Montagem do Drive e Carregamento dos Dados                     | Mensagem de sucesso e exibição de `df.head()`            |
| 5      | Transformação (Encoding e Shuffle) e Divisão (Treino/Teste)    | Exibição dos tamanhos finais dos subconjuntos            |
| 7      | Treinamento e Avaliação                                        | Exibição da Acurácia e do gráfico de Matriz de Confusão  |
| 9      | Predição de Teste                                              | Exibição da classificação final (UNACC, ACC, GOOD, VGOOD) |
