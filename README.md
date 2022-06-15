# Título
Classificação de Imagens de Raio-X

# Objetivo

Neste trabalho temos por objetivo classificar imagens de acordo com a região do corpo humano que ela representa. 
Para isso, serão utilizadas imagens disponíveis em uma competição chamada UNIFESP X-ray Body Part Classifier Competition aberta até Agosto de 2022 na plataforma Kaggle.

https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier

## Conteúdos utilizados

* Image Enhancement;
* Image Segmentation;
* Image Filtering;
* Image Description.

conhecimentos de Image Enhancement, Segmentation e Filtering serão utlizados para pré-processar as imagens e com isso aplicar o algortimo de Bag of Features para a classificação das imagens de teste.

# Exemplos de Imagem de Input

![Pulmão](/Imagens/Pulmão.png)

![Diversos](/Imagens/Diversos.png)


# Aplicação

Embora pareça uma tarefa inútil para aplicações práticas, a identificação automática de diferentes partes do corpo humano segundo uma imagem de raio X pode ser a chave para a automatização completa de sistemas hospitalares.

Em muitos hospitais, quando um médico receita diversos exames de raio X diferentes, o programa de computador, embora crie os campos desejados, como por exemplo, "joelho", "perna", "bacia", não é capaz de identificar quais imagens de raio X obtidas representam cada classe, deixando isso a cargo do operador da máquina. O problema se intensifica a medida que a quantidade de imagens de raio X aumenta. Logo, é importante criar um modelo que faça a classificação dessas imagens ao invés de ser algo manual. Apesar disso, a presença de imagens erradas no conjunto de treinamento pode levar a problemas na eficácia com relação à detecção dessas doenças.

Assim, a ideia de construirmos um modelo para a classificação de diferentes partes do corpo a partir de imagens de raio X tem por objetivo ser uma forma de organização e preparação das imagens para projetos maiores.
