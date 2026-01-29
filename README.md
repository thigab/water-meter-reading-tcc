# Detecção e Reconhecimento de Dígitos em Hidrômetros com Modelos de
Aprendizado de Máquina

[![Status](https://img.shields.io/badge/Status-Concluído_(TCC)-success?style=for-the-badge)](https://github.com/thigab/water-meter-reading-tcc)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge)](https://www.python.org/)

## Contexto Acadêmico
Este repositório contém os artefatos desenvolvidos no âmbito do **Trabalho de Conclusão de Curso (TCC)** do Bacharelado em Ciências Exatas e Tecnológicas (BCET).

O projeto propõe uma solução baseada em **Visão Computacional** e **Deep Learning** para a leitura automática de hidrômetros em imagens reais, superando desafios de iluminação e enquadramento.

## Documentação
A fundamentação teórica e os detalhes metodológicos estão disponíveis nos documentos abaixo:

* [**Monografia Completa (PDF)**](docs/TCC_Thiago_Oliveira.pdf)
* **Artigo Científico:** *Em fase de escrita e revisão.*

---

## Arquitetura da Solução
A abordagem foi dividida em um pipeline de dois estágios para garantir maior robustez:

1.  **Detecção e Segmentação:** Localização automática da região do visor (ROI - Region of Interest).
2.  **Classificação Numérica:** Identificação dos dígitos individuais a partir das regiões recortadas.

### Estrutura dos Notebooks

| Arquivo | Descrição e Link |
| :--- | :--- |
| `Segmentação_detecção.ipynb` | **Etapa 1:** Realiza o pré-processamento e identifica a região do visor do hidrômetro. O output deste modelo recorta a área onde os dígitos estão presentes. <br> [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thigab/water-meter-reading-tcc/blob/main/notebooks/Segmenta%C3%A7%C3%A3o_detec%C3%A7%C3%A3o.ipynb) |
| `modelo_de_classificacao_balanceada.ipynb` | **Etapa 2:** Classifica os dígitos numéricos recortados. **Destaque:** Utiliza técnicas de junção de datasets e balanceamento de classes para ampliar a diversidade e robustez do treinamento. <br> [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/thigab/water-meter-reading-tcc/blob/main/notebooks/modelo_de_classificacao_balanceada.ipynb) |

---

## Resultados Visuais

### 1. Pré-processamento e Segmentação
Visualização da detecção da área do medidor.
![Resultado Segmentação](assets/resultado_segmentacao.png)

### 2. Classificação dos Dígitos
Exemplo de inferência do modelo nos dígitos isolados.
![Resultado Classificação](assets/resultado_classificacao.png)

---

## Roadmap (Próximos Passos)
O projeto segue em evolução para portabilidade e aplicação em dispositivos móveis:

- [x] Desenvolvimento e validação dos modelos (TCC)
- [ ] Otimização de hiperparâmetros
- [ ] **Versão Mobile com TensorFlow Lite** (Reservado para futura implementação Android)

## Tecnologias
* **Linguagem:** Python
* **Deep Learning:** TensorFlow / Keras
* **Processamento de Imagem:** OpenCV
* **Ambiente:** Google Colab

## Autor
Desenvolvido por **Thiago Gabriel Da Silva Oliveira**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/thigab)
