# Classificação de Letras Manuscritas: Detecção da Letra "i"

Projeto de classificação binária de imagens de vogais manuscritas para identificar se a letra é "i" ou outra vogal (a, e, o, u).

## Sobre o Projeto

- **Objetivo**: Classificar imagens de vogais manuscritas como "i" ou "não-i"
- **Dataset**: 10.000 imagens em escala de cinza, redimensionadas para 16×16 pixels (vetores de 256 features)
- **Modelos avaliados**: KNN (k=3), MLP (1 camada oculta, 100 neurônios) e Random Forest (100 árvores)
- **Validação**: 3-fold stratified cross-validation

## Resultados

| Modelo         | Acurácia | F1-Score | Precisão | Revocação |
|----------------|----------|----------|----------|-----------|
| Random Forest  | 98.34%   | 95.78%   | 97.42%   | 94.19%    |
| KNN (k=3)      | 96.96%   | 92.68%   | 93.10%   | 92.26%    |
| MLP            | 91.85%   | 76.27%   | 73.38%   | 79.38%    |

## Requisitos

- Python ≥ 3.9
- Bibliotecas listadas em `requirements.txt`

## Dataset

O notebook espera o dataset de vogais manuscritas em `imagens/indie/pi/dataset/v20220930/` (o diretório `imagens/` está no `.gitignore` e não é versionado).

- **Estrutura esperada**: uma subpasta por vogal (`a`, `e`, `i`, `o`, `u`), cada uma com as imagens em escala de cinza (PNG/JPG/JPEG)
- **Como usar**: baixe/extraia o dataset e organize-o conforme o caminho `DATA_DIR` definido no notebook (`letters.ipynb`, célula de configuração)

## Uso

```bash
pip install -r requirements.txt
jupyter notebook letters.ipynb
```
