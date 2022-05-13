# Título
Classificação de Imagens de Raio-X

# Objetivo


Neste trabalho temos por objetivo classificar imagens de acordo com a região do corpo humano que ela representa. 
Para isso, serão utilizadas imagens disponíveis em uma competição chamada UNIFESP X-ray Body Part Classifier Competition aberta até Agosto de 2022 na plataforma Kaggle.

## Conteúdos utilizados

* Image Enhancement;
* Image Segmentation;
* Image Filtering;
* Redes Neurais.

conhecimentos de Image Enhancement, Segmentation e Filtering serão utlizados para pré-processar as imagens e com isso aplicar algoritmos de Redes Neurais para a classificação das mesmas.

# Exemplos de Imagem de Input

![Pulmão](/Imagens/Pulmão.png)

![Diversos](/Imagens/Diversos.png)


# Aplicação

Embora pareça uma tarefa inútil para aplicações práticas, a identificação automática de diferentes partes do corpo humano segundo uma imagem de raio X pode ser a chave para a automatização completa de sistemas hospitalares.

Em muitos hospitais, quando um médico receita diversos exames de raio X diferentes, o programa de computador, embora crie os campos desejados, como por exemplo, "joelho", "perna", "bacia", não é capaz de identificar quais imagens de raio X obtidas representam cada classe, deixando isso a cargo do operador da máquina. O problema se intensifica bastante quando pensamos em grande quantidades de imagens de raio X usadas para treinamento de inteligências artificiais dedicadas à detecção de doenças específicas por exemplo. A presença de imagens erradas no conjunto de treinamento podem levar a discrepâncias muito altas para a eficácia da detecção dessas doenças.

Assim, a ideia de construirmos uma rede para a classificação de diferentes partes do corpo a partir de imagens de raio X vem como uma forma de organização e preparação de dados para projetos maiores. A inspiração do projeto vem da competição em aberto da plataforma de machine learning Kaggle:

https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier
