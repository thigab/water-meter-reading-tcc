# Notebooks – Projeto TCC (BCET)

Este diretório contém os notebooks desenvolvidos no contexto do
Trabalho de Conclusão de Curso do Bacharelado em Ciências Exatas e Tecnológicas (BCET).

O projeto tem como objetivo o desenvolvimento de uma solução baseada em
Visão Computacional e Deep Learning para leitura automática de hidrômetros,
utilizando uma abordagem em duas etapas: localização da região de interesse
e classificação dos dígitos numéricos.

## Descrição Geral da Solução

A solução proposta é composta por dois modelos principais:

1. Um modelo de **segmentação/detecção**, responsável por localizar
automaticamente a região do visor (relógio) do hidrômetro nas imagens.

2. Um modelo de **classificação**, responsável por identificar e classificar
os dígitos numéricos presentes na região do visor, a partir das imagens já recortadas.

Ambos os modelos incluem etapas de pré-processamento de imagens,
treinamento, validação e análise de desempenho.

## Conteúdo

- **Segmentação_detecção.ipynb**  
  Notebook responsável pelo desenvolvimento do modelo de segmentação/detecção de imagens.
  Este modelo realiza o pré-processamento dos dados e identifica a região do visor
  do hidrômetro, delimitando a área onde os dígitos numéricos estão presentes.
  O resultado deste modelo é utilizado como etapa anterior ao processo de classificação.

- **modelo_de_classificacao_balanceada.ipynb**  
  Notebook responsável pelo desenvolvimento do modelo de classificação dos dígitos
  numéricos do hidrômetro. As imagens utilizadas neste notebook correspondem às regiões
  previamente recortadas a partir do modelo de segmentação.
  Para aumentar a robustez do treinamento, foi realizada a junção de diferentes datasets,
  bem como técnicas de balanceamento de classes, visando ampliar a quantidade e a
  diversidade das imagens utilizadas.

## Contexto Acadêmico

Os notebooks apresentados fazem parte de uma pesquisa aplicada em Visão Computacional,
desenvolvida no âmbito do Trabalho de Conclusão de Curso.
Os experimentos foram implementados utilizando técnicas de Deep Learning,
com execução e testes realizados em ambiente Google Colab.
