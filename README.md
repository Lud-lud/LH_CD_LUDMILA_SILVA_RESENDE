## Análise e previsão de preços de aluguéis em Nova York

Este projeto desenvolvido durante o processo seletivo para o Programa Lighthouse da Indicium, uma formação de 6 meses gratuita e completa em dados.

---

### Análise exploratória dos dados

Foram realizados boxplots, tabelas e mapas para analisar a relação entre as variáveis, que podem ser visualizados no notebook principal
[(desafio_ciencia_de_dados_2025_3.ipynb)](https://github.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/blob/main/desafio_ciencia_de_dados_2025_3.ipynb).

Importante alertar que o mapa perceptual resultante da análise de correspondência múltipla, por ser uma visualização dinâmica 3D, não foi renderizado no arquivo 
desafio_ciencia_de_dados_2025-3.ipynb. Sendo assim,
sua visualização somente será possível caso o notebook seja rodado novamente em alguma IDE, de preferência o Colab.
O mapa perceptual deve se parecer com esta figura:

<img src='https://raw.githubusercontent.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/refs/heads/main/mapa_perceptual.png' />

---

### Modelagem preditiva

Foram testados quatro modelos preditivos: regressão linear múltipla, árvore de regressão, random forest e XGBoost, sendo este último o que apresentou a melhor performance dentre todos,
com erro quadrático absoluto médio de 9,39 e R² de 62,53%.

Foi realizada a transformação de Box-Cox na variável resposta 'price' devido a não-normalidade 
de sua distribuição, o que melhorou o ajuste dos modelos.
Com esta transformação, o output do modelo precisa ser
multiplicado pelo valor de lambda gerado para que ele volte à escala original.

A previsão pode ser feita diretamente no 
[notebook principal](https://github.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/blob/main/desafio_ciencia_de_dados_2025_3.ipynb)
ou no arquivo de
[teste do modelo](https://github.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/blob/main/teste_modelo.ipynb), bastando para o segundo caso ter carregado o arquivo .pkl do
[Modelo XGBoost](https://github.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/blob/main/modelo_xgboost.pkl).

---
### Arquivos associados

Dados de input: [teste_indicium_precificacao.csv](https://github.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/blob/main/teste_indicium_precificacao)

Arquivo de requisitos: [requirements.txt](https://github.com/Lud-lud/LH_CD_LUDMILA_SILVA_RESENDE/blob/main/requirements.txt)
