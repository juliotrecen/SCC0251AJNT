# Título
Classificação de Imagens de Raio-X

# Objetivo

Neste trabalho temos por objetivo comparar como diferentes formas de pré-processamento de imagens pode ajudar na classificação de imagens de acordo com a região do corpo humano que ela representa. Para o pré-processamento das imagens serão utilizados conhecimentos de Image Enhancement, Segmentation e Filtering, já para a classificação será  utilizado o algoritmo de Bag of Features (BoF).
As imagens utilizadas neste projetos serão as disponíveis em uma competição chamada UNIFESP X-ray Body Part Classifier Competition que está aberta até Agosto de 2022 na plataforma Kaggle.

Link da competição: https://www.kaggle.com/competitions/unifesp-x-ray-body-part-classifier

## Conteúdos utilizados

* Image Enhancement;
* Image Segmentation;
* Image Filtering;
* Image Description.

conhecimentos de Image Enhancement, Segmentation e Filtering serão utlizados para pré-processar as imagens e com isso aplicar o algortimo Bag of Features para a classificação das mesmas.

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

# Como alcançar nosso objetivo (Metodologia)

As imagens fornecidas no Kaggle estão no formato DCIM, para facilitar nosso trabalho, primeiro transformamos elas em JPG.

Como dito acima, nosso objetivo é estudar diversos formas de pré-processamento de imagens e como isso auxilia na classificação de imagens de raio-x. Para isso, primeiro criamos alguns tipos de image enhencement, neste caso criamos uma função no python que de acordo com as configurações de seus argumento aplica 3 tipos diferentes de image enhancement nas imagens.
Na sequência, utilizamos um conjunto de treino providenciado na competição do Kaggle para criar um dicionário do algoritmo Bag of Features. Com isso, selecionamos imagens na base de teste e verificamos quais as imagens da base de treino que mais se aproximam da selecionada. Tendo isso, observamos de qual parte do corpo a maioria das imagens de treino fazem parte e assim classificamos a imagem de teste.
A ideia do trabalho é aplicar diversos filtros em uma mesma imagem de teste e verificar com quais filtros a classificação da imagem foi correta.


# Resultados preliminares

Criamos três filtros para aplicar na imagem e tentar auxiliar na classificação de imagens de teste. Segue abaixo o resultado ao aplicar esses filtros e as imagens de treino mais próximas da de teste (imagem de uma mão)

### Método 0 - Sem filtro (original)

![Preliminar_Original](/Imagens/Preliminar_Original.jpeg)

Quando não aplica-se filtro, apenas o algoritmo BoF sem pré-processamento, observa-se um resultado satisfatório, já que cinco de oito fotos foram de mãos mesmo elas não estando com o mesmo posicionamento na foto e as outras imagens foram de partes próximas (dedo da mão, pulso) ou de estrutura similar (pé).

### Método 1 - Binary

![Preliminar_Binary](/Imagens/Preliminar_Binary.jpeg)

Quando aplica-se o filtro binário há uma piora no resultado do algoritmo BoF. Apenas 1 imagem de treino é de uma mão e várias imagens ditas "próximas" da imagem de teste são de estruturas do corpo humano muito diferente (pulmão, braço e lombar).
