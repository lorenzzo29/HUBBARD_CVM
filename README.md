# HUBBARD_CVM

**Cluster Variation Methods for Fermions on the Lattice – Mathematical Foundations and Application to the Hubbard Model**

Este repositório contém o código desenvolvido para a dissertação de mestrado intitulada:

> _"Métodos de Variação de Cluster para Férmions na Rede – Fundamentos Matemáticos e Aplicação ao Modelo de Hubbard"_

Resumo da Dissertação:

Nesta dissertação, desenvolvemos uma abordagem matemática para a mecânica estatística quântica aplicada em modelos com Interações de Curto Alcance, por exemplo, o modelo de Hubbard, em redes bidimensionais, através do uso do Método da Variação de Clusters (CVM), a qual prova a convergência do Método CVM para o caso quântico, estendendo os resultados previamente desenvolvidos para modelos de spins clássicos.

Os modelos de campo médio, como o modelo de Curie-Weiss para sistemas clássicos, fornecem uma primeira aproximação para a descrição de transições de fase ferromagnéticas. No entanto, sua simplicidade decorre da negligência das interações locais e da correlação entre sítios próximos. O CVM oferece uma alternativa mais precisa, incorporando interações locais de forma sistemática.

Nesta pesquisa, adaptamos a abordagem formal do CVM clássico ao contexto quântico, e assim foi possível provar que o CVM é capaz de produzir a pressão e o estado de equilíbrio exatos, à medida que aumentamos o tamanho dos seus clusters, bem como a convergência da energia livre no limite termodinâmico.


Abstract:

In this dissertation, we develop a mathematical approach to quantum statistical mechanics applied to models with short-range interactions, such as the Hubbard model, on two-dimensional lattices, through the use of the Cluster Variation Method (CVM). This formulation proves the convergence of the CVM in the quantum case, thus extending previous results originally established for classical spin models.

Mean-field models, such as the Curie-Weiss model for classical systems, provide a first approximation for describing ferromagnetic phase transitions. However, their simplicity arises from neglecting local interactions and correlations between neighboring sites. The CVM offers a more accurate alternative by systematically incorporating local interactions.

In this work, we adapt the formal structure of the classical CVM to the quantum context, and we show that the CVM is capable of producing the exact pressure and equilibrium state as the cluster size increases, as well as ensuring the convergence of the free energy in the thermodynamic limit.


**Autor**: Lorenzzo V. S. Delmutti  
**Orientador**: Prof. Dr. Walter Alberto de Siqueira Pedra  
**Programa**: Pós-Graduação em Física – Instituto de Física da Universidade de São Paulo (IFUSP)

---

## Descrição da Simulação Numérica

Implementação do **Método de Variação de Clusters (CVM)** aplicado ao **modelo de Hubbard 2D** com interações de curto alcance. O código realiza:

- Construção de matrizes densidade variacionais para clusters de 1, 2 e 4 pontos.
- Cálculo da energia, entropia de von Neumann e energia livre com fórmula de Möbius.
- Minimização da energia livre total com penalizações de consistência entre subclusters.
- Simulações otimizadas para CPU, com paralelização via `joblib`.
- Geração de tabelas com resultados físicos como E, S, e F por sítio.

---

## Estrutura do Código Computacional

Embora esteja atualmente em um único arquivo, o código pode ser dividido logicamente nos seguintes módulos:

| Bloco Funcional              | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| **Execução principal**       | Gera a curva F(T) variando a temperatura, com paralelização via Joblib |
| **Hamiltonianos**            | Construção dos operadores H_1, H_2, H_4 do modelo de Hubbard |
| **Funções de CVM**           | Parametrização de rho, entropia de von Neumann, traço parcial, etc. |
| **Minimizador**              | Minimização variacional com LBFGS e penalizações de consistência         |
| **Utilitários**              | Inicialização de parâmetros, verificação de estabilidade, etc.           |

---

## Parâmetros 

No código, CVM aproximação quadrada 2 X 2 para o Modelo de Hubbard, os parâmetros utilizados foram as seguintes:


- t (hopping): unidade de energia, medido em eV, com t = 0.4.
- U (interação local): unidade de energia, medido em eV, com U = 3.0.
- mu (potencial químico): unidade de energia, medido em eV, com mu = 1.0.


## Contato

Para dúvidas ou colaborações, entre em contato:  
lorenzzo.lvsd@usp.br  
lorenzzo.lvsd@gmail.com



## Citação

Se este código for útil para sua pesquisa, por favor cite:

> Delmutti, L. (2025). _Métodos de Variação de Cluster para Férmions na Rede – Fundamentos Matemáticos e Aplicação ao Modelo de Hubbard_. Dissertação de Mestrado, Instituto de Física da Universidade de São Paulo.


## Requisitos

- Python ≥ 3  
- Instale as bibliotecas necessárias com:

```bash
pip install torch numpy matplotlib scipy joblib pandas tqdm

