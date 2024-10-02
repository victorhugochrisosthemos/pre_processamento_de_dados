# Pré-processamento de Dados para Aplicação em Algoritmos de Machine Learning
- Estudo sobre maneiras de lidar com os dados antes de realizar o aprendizado de máquina<br>
- Aulas do Doutor Jones Granatyr<br>
- Utilizado como exercício duas bases de dados
    - credit_data.csv
    - census.csv
- Exercícios realizados em python no Google Colab
    - Base de dados do Censo
    - Tendência de pagamento de empréstimo

## Tipos de Dados
- O primeiro cuidado a ser considerado é sobre o tipo de variáveis que possuímos
- Classificações:
    - Numéricas: possui números
        - Contínuas(float): valores do conjunto dos reais como idade, altura, peso
        - Discretas(int): valores do conjunto dos inteiros como quantidade de matérias na faculdade
    - Categóricas: possui letras
        - Nominais: valores não mensuráveis como gênero, cor dos cabelos
        - Ordinais: valores com ordenação como tamanho da camisa(P, M e G)

## Outliers
- Outliers são dados que se diferenciam drasticamente de todos os outros.
- É um valor que foge da normalidade e que pode causar anomalias nos resultados obtidos por meio de algoritmos.
- Um exemplo é a altura de um grupo de pessoas, se a maioria das alturas variam entre 1,60 e 1,80 metros, a medida de uma pessoa com 2,50m é um outlier, que está muito fora do padrão normal do grupo.

## Escalonamento/Padronização de Valores
![image](https://github.com/user-attachments/assets/875a99a6-8142-4e34-850d-81c79bb49a50)

- Uma técnica para ajsutar a escala dos valores das variáveis
- A padronização transforma as variáveis para que tenham uma média de 0 e desvio-padrão de 1, tornando-as comparáveis, mesmo que tenha escalas muito diferentes.
- Melhor para modelos lineares.
## Normalização de Valores
- Uma técnica para ajsutar a escala dos valores das variáveis
- Coloca os dados em uma faixa específica (ex.: [0, 1]), usada quando é necessário garantir que todas as variáveis tenham o mesmo peso.
- Melhor para modelos baseados em distâncias(KNN, Redes Neurais).
## LabelEncoder
- Técnica para transformar valores categóricos em número
- Exemplo: tamanho de camisa em pequeno, médio e grande. Com o LabelEncoderfica assim:
    - Pequeno → 0
    - Médio → 1
    - Grande → 2
## OneHotEnconder
- Técnica usada para converter valore categóricos nominais em representação numérica.
- O OneHotEncoder evita que o modelo aprenda uma "hierarquia inexistente" entre os valores nominais.
- Um exemplo, ao considerar os possíveis valores entre 0, 1 e 2, é possível que o algoritmo entenda que a classe 2 é “maior” ou “mais importante” que a classe 1, interferindo negativamente na aprendizagem.
- Cada valor de uma variável categórica vira várias colunas binárias, para um valor na matrix somente uma das colunas será preenchido.
  
