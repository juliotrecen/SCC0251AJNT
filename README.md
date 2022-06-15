# Título
Classificação de Imagens de Raio-X

# Objetivo

Neste trabalho temos por objetivo comparar como diferentes formas de pré-processamento de imagens pode ajudar na classificação de imagens de acordo com a região do corpo humano que ela representa. Para o pré-processamento das imagens serão utilizados conhecimentos de Image Enhancement, Segmentation e Filtering, já para a classificação será  utilizado o algoritmo de Bag of Features.
As imagens utilizadas neste projetos serão as disponíveis em uma competição chamada UNIFESP X-ray Body Part Classifier Competition que está aberta até Agosto de 2022 na plataforma Kaggle.

Link da competição: https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier

## Conteúdos utilizados

* Image Enhancement;
* Image Segmentation;
* Image Filtering;
* Image Description.

conhecimentos de Image Enhancement, Segmentation e Filtering serão utlizados para pré-processar as imagens e com isso aplicar o algortimo de Bag of Features para a classificação das mesmas.

# Imagens de Input

As imagens utilizadas neste projeto são imagens de raio-x que compreendem 24 regiões do corpo humando, sendo elas:

Abdômem, tornozelo, coluna cervical, peito, clavículas, cotovelo, pés, dedo, antebraço, mão, quadril, joelho, perna, lombar, outros, pelve, ombro, seio, crânio, coxa, coluna torácica e pulso.

Alguns exemplos de imagens que aparecem no dataset:

![Pulmão](/Imagens/Pulmão.png)

![Diversos](/Imagens/Diversos.png)


# Aplicação

Embora pareça uma tarefa inútil para aplicações práticas, a identificação automática de diferentes partes do corpo humano segundo uma imagem de raio X pode ser a chave para a automatização completa de sistemas hospitalares.

Em muitos hospitais, quando um médico receita diversos exames de raio X diferentes, o programa de computador, embora crie os campos desejados, como por exemplo, "joelho", "perna", "bacia", não é capaz de identificar quais imagens de raio X obtidas representam cada classe, deixando isso a cargo do operador da máquina. O problema se intensifica a medida que a quantidade de imagens de raio X aumenta. Logo, é importante criar um modelo que faça a classificação dessas imagens ao invés de ser algo manual. Apesar disso, a presença de imagens erradas no conjunto de treinamento pode levar a problemas na eficácia com relação à detecção dessas doenças.

Assim, a ideia de construirmos um modelo para a classificação de diferentes partes do corpo a partir de imagens de raio X tem por objetivo ser uma forma de organização e preparação das imagens para projetos maiores.
