# Estimativa de Profundidade em Imagens 2D para Geração de Efeitos Visuais

## Autores
        # - Felipe U. G. de Sousa (RA: 10418415)
        # - Gustavo N. Siqueira (RA: 10419057)
        # - Thomaz de S. Scopel (RA: 10417183)
        # - Vinicius S. Cappatti (RA: 10418266)

---

## Introdução

A geração de efeitos de profundidade a partir de imagens bidimensionais tem se tornado um tema relevante na área de Computação Visual, especialmente com o avanço de técnicas baseadas em aprendizado de máquina. Tradicionalmente, a percepção de profundidade depende de múltiplas imagens ou sensores especializados, como câmeras estéreo ou sensores LiDAR. No entanto, abordagens modernas permitem inferir profundidade a partir de uma única imagem, utilizando modelos de redes neurais profundas.

Esse problema é conhecido como **Monocular Depth Estimation**, e possui diversas aplicações, incluindo realidade aumentada (AR), realidade virtual (VR), efeitos visuais, fotografia computacional (modo retrato) e interfaces interativas.

---

## Referencial Teórico

Um dos trabalhos recentes relevantes nessa área é o artigo *“Generating Spatial Images using Monocular Depth Estimation”* (2024), que propõe um pipeline para transformar imagens 2D em representações com profundidade estimada.

Disponível em:  
https://cs231n.stanford.edu/2024/papers/generating-spatial-images-using-monocular-depth-estimation.pdf

O método apresentado no artigo consiste em duas etapas principais:

### 1. Estimativa de Profundidade

Inicialmente, um modelo de aprendizado profundo é utilizado para prever um **mapa de profundidade (depth map)** a partir de uma imagem RGB. Esse mapa representa a distância relativa de cada pixel em relação à câmera.

Essa abordagem utiliza arquiteturas modernas como redes convolucionais (CNNs) e modelos baseados em codificador-decodificador (encoder-decoder), permitindo extrair informações espaciais complexas mesmo sem dados explícitos de profundidade.

### 2. Geração de Efeitos de Profundidade

Com o mapa de profundidade gerado, é possível aplicar diferentes efeitos visuais, tais como:

- Efeito de paralaxe (parallax)
- Desfoque de fundo (bokeh)
- Geração de imagens estereoscópicas (visão esquerda/direita)
- Simulação de movimento 3D

Esses efeitos criam a ilusão de tridimensionalidade a partir de uma única imagem, ampliando significativamente as possibilidades de aplicação.

---

## Aplicação no Projeto

No contexto deste projeto, a proposta consiste em aplicar técnicas de estimativa de profundidade para gerar efeitos visuais em imagens estáticas. A ideia central é:

1. Receber uma imagem 2D como entrada  
2. Gerar um mapa de profundidade utilizando um modelo pré-treinado  
3. Aplicar transformações visuais com base nesse mapa  
4. Produzir uma saída com efeito de profundidade (ex: parallax ou desfoque)

Essa abordagem está diretamente alinhada com o estado da arte apresentado na literatura recente, demonstrando a viabilidade prática do uso de inteligência artificial para tarefas de computação visual.

---

## Considerações Finais

A estimativa de profundidade a partir de imagens monoculares representa um avanço significativo na área de visão computacional. A possibilidade de extrair informações tridimensionais de dados bidimensionais amplia o escopo de aplicações e reduz a dependência de hardware especializado.

Com base no artigo analisado, observa-se que técnicas modernas conseguem produzir resultados convincentes, tornando essa abordagem adequada para implementação em projetos acadêmicos e aplicações reais.

---

## Referências

SOIN, Karan et al. *Generating Spatial Images using Monocular Depth Estimation*. Stanford University, 2024.  
Disponível em: https://cs231n.stanford.edu/2024/papers/generating-spatial-images-using-monocular-depth-estimation.pdf

---
