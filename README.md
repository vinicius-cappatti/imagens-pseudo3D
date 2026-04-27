# Estimativa de Profundidade em Imagens 2D para Geração de Efeitos Visuais

## Autores
- Felipe U. G. de Sousa (RA: 10418415)
- Gustavo N. Siqueira (RA: 10419057)
- Thomaz de S. Scopel (RA: 10417183)
- Vinicius S. Cappatti (RA: 10418266)

---

## Introdução

A geração de efeitos de profundidade a partir de imagens bidimensionais tem se tornado um tema relevante na área de Computação Visual, especialmente com o avanço de técnicas baseadas em aprendizado de máquina. Tradicionalmente, a percepção de profundidade depende de múltiplas imagens ou sensores especializados, como câmeras estéreo ou sensores LiDAR. No entanto, abordagens modernas permitem inferir profundidade a partir de uma única imagem, utilizando modelos de redes neurais profundas.

Esse problema é conhecido como **Monocular Depth Estimation**, e possui diversas aplicações, incluindo realidade aumentada (AR), realidade virtual (VR), efeitos visuais, fotografia computacional (modo retrato) e interfaces interativas.

---

## Referencial Teórico

Um dos trabalhos recentes relevantes nessa área é o artigo:

**Generating Spatial Images using Monocular Depth Estimation (2024)**  
https://cs231n.stanford.edu/2024/papers/generating-spatial-images-using-monocular-depth-estimation.pdf

Esse trabalho propõe um pipeline que combina estimativa de profundidade com técnicas de geração de imagens estereoscópicas, utilizando efeitos como parallax e bokeh para criar sensação de profundidade em imagens 2D :contentReference[oaicite:0]{index=0}.

---

## Trabalhos Relacionados

### 1. Monocular Depth Estimation (Fundamentos)

Um dos trabalhos clássicos na área é:

**3-D Depth Reconstruction from a Single Still Image**  
https://www.cs.cornell.edu/~asaxena/learningdepth/ijcv_monocular3dreconstruction.pdf

Esse estudo demonstra que é possível estimar profundidade a partir de uma única imagem utilizando aprendizado supervisionado e modelagem de relações espaciais entre regiões da imagem :contentReference[oaicite:1]{index=1}.

Ele introduz conceitos fundamentais que servem de base para métodos modernos.

---

### 2. Survey moderno de Monocular Depth Estimation

**Monocular Metric Depth Estimation Survey (2025)**  
https://arxiv.org/html/2501.11841v1

Esse trabalho apresenta um panorama atualizado da área, destacando que modelos modernos utilizam redes neurais profundas para inferir profundidade diretamente de imagens RGB, sem necessidade de sensores adicionais :contentReference[oaicite:2]{index=2}.

Além disso, reforça aplicações como:
- reconstrução 3D
- navegação autônoma
- geração de novas visualizações

---

### 3. Pseudo-3D e Parallax

Técnicas de pseudo-3D utilizam mapas de profundidade para simular tridimensionalidade a partir de imagens 2D.

O conceito de **2D + Depth** consiste em associar uma imagem a um mapa de profundidade, permitindo gerar múltiplas visualizações e criar efeito tridimensional :contentReference[oaicite:3]{index=3}.

Além disso, técnicas como **parallax** exploram a variação de perspectiva para criar sensação de profundidade, sendo amplamente utilizadas em animações e visualizações interativas :contentReference[oaicite:4]{index=4}.

---

## Metodologia Proposta

O projeto segue um pipeline baseado no estado da arte:

### 1. Entrada
- Imagem RGB (2D)

### 2. Estimativa de profundidade
- Uso de modelo pré-treinado de monocular depth estimation
- Geração de um **depth map**, onde cada pixel representa a distância relativa

### 3. Processamento do depth map
- Normalização
- Suavização
- Ajuste de contraste de profundidade

### 4. Aplicação de efeitos

A partir do depth map, são aplicados:

- Parallax (movimento de câmera simulado)
- Blur seletivo (bokeh)
- Pseudo-3D (deslocamento de camadas)
- Geração de múltiplas perspectivas

---

## Aplicações

- Realidade aumentada (AR)
- Realidade virtual (VR)
- Fotografia computacional
- Edição de imagens
- Interfaces interativas
- Jogos e animações

---

## Considerações Finais

A estimativa de profundidade monocular representa uma solução eficiente e de baixo custo para geração de efeitos tridimensionais a partir de imagens 2D.

Com o avanço de redes neurais profundas, tornou-se possível inferir estrutura espacial de forma convincente, permitindo aplicações práticas em diversos contextos.

Os trabalhos analisados demonstram que a combinação de:
- depth estimation
- parallax
- pseudo-3D

é suficiente para criar experiências visuais imersivas sem necessidade de hardware especializado.

---

## Referências

SOIN, Karan et al.  
*Generating Spatial Images using Monocular Depth Estimation*. Stanford, 2024.  
https://cs231n.stanford.edu/2024/papers/generating-spatial-images-using-monocular-depth-estimation.pdf  

SAXENA, Ashutosh; CHUNG, Sung; NG, Andrew.  
*3-D Depth Reconstruction from a Single Still Image*.  
https://www.cs.cornell.edu/~asaxena/learningdepth/ijcv_monocular3dreconstruction.pdf  

ZHANG, J. et al.  
*Monocular Metric Depth Estimation Survey*, 2025.  
https://arxiv.org/html/2501.11841v1  

---
