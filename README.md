# Processamento de imagens 2D com efeito pseudo‑3D

Este repositório contém um **notebook Jupyter** (`execucao_final.ipynb`) que demonstra um pipeline simples para gerar **efeito de paralaxe (pseudo‑3D)** a partir de **uma única imagem 2D**, usando um **mapa de “profundidade” sintético** (gerado matematicamente) e a operação de **remapeamento** de pixels (`cv2.remap`, OpenCV).

## Autores
- Felipe U. G. de Sousa (RA: 10418415)
- Gustavo N. Siqueira (RA: 10419057)
- Thomaz de S. Scopel (RA: 10417183)
- Vinicius S. Cappatti (RA: 10418266)

---

## Como o repositório está organizado

- **`execucao_final.ipynb`**: notebook principal (seção teórica + seção prática + interface interativa com sliders).
- **`requirements.txt`**: dependências Python necessárias para executar o notebook.
- **`imgs/`**: imagens usadas pelo próprio notebook/README (ex.: figura ilustrativa de DIBR).

---

## Como o notebook funciona (visão geral)

Na seção prática do notebook, o pipeline segue esta ideia:

- **Leitura e redimensionamento**: carrega uma imagem (`cv2.imread`) e limita o tamanho para facilitar a interação.
- **Mapa de profundidade sintético**: como não é estimado por rede neural neste projeto, o notebook cria um mapa “tipo colina” (maior no centro, menor nas bordas) e o converte em deslocamentos máximos em pixels.
- **Pseudo‑3D via DIBR simplificado**: para cada posição dos sliders (`dx`, `dy`), calcula mapas `mapa_x` e `mapa_y` e aplica `cv2.remap` para produzir a imagem “deslocada”, gerando a sensação de paralaxe.
- **Interface interativa**: `ipywidgets` cria sliders para controlar o deslocamento e atualizar a imagem em tempo real.

---

## Como executar o notebook

### Pré‑requisitos
- **Python 3.10+** (recomendado)
- Jupyter Notebook/Lab (o `requirements.txt` já inclui `ipykernel`)

### Passo a passo (Windows / PowerShell)

1) Crie e ative um ambiente virtual (opcional, mas recomendado):

```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2) Instale as dependências:

```bash
python -m pip install -r requirements.txt
```

3) Inicie o Jupyter:

```bash
jupyter lab
```

4) Abra o arquivo `execucao_final.ipynb` e execute as células **na ordem**.

### Configuração da imagem de entrada (importante)

No notebook, a variável `caminho_da_imagem` precisa apontar para uma imagem válida. Para facilitar a execução em qualquer máquina, **prefira usar um caminho relativo**, por exemplo:

```python
caminho_da_imagem = "inputs/cachorro-gravata.jpg"
```

Se você usar caminho absoluto, outras pessoas não conseguirão rodar o notebook sem editar esse valor.
