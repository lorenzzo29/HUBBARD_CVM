# HUBBARD_CVM

**Cluster Variation Methods for Fermions on the Lattice – Mathematical Foundations and Application to the Hubbard Model**

Este repositório contém o código desenvolvido para a dissertação de mestrado intitulada:

> _"Cluster Variation Methods for Fermions on the Lattice – Mathematical Foundations and Application to the Hubbard Model"_

**Autor**: Lorenzzo V. S. Delmutti  
**Orientador**: Prof. Dr. Walter Alberto de Siqueira Pedra  
**Programa**: Pós-Graduação em Física – Instituto de Física da Universidade de São Paulo (IFUSP)

---

## Descrição

Implementação do **Método de Variação de Clusters (CVM)** aplicado ao **modelo de Hubbard 2D** com interações de curto alcance. O código realiza:

- Construção de matrizes densidade variacionais para clusters de 1, 2 e 4 pontos.
- Cálculo da energia, entropia de von Neumann e energia livre com fórmula de Möbius.
- Minimização da energia livre total com penalizações de consistência entre subclusters.
- Simulações otimizadas para CPU, com paralelização via `joblib`.
- Geração de tabelas com resultados físicos como \( E \), \( S \), e \( F \) por sítio.

---

## Estrutura do Código

Embora esteja atualmente em um único arquivo, o código pode ser dividido logicamente nos seguintes módulos:

| Bloco Funcional              | Descrição                                                                 |
|-----------------------------|---------------------------------------------------------------------------|
| **Execução principal**       | Gera a curva \( F(T) \) variando a temperatura, com paralelização via Joblib |
| **Hamiltonianos**            | Construção dos operadores \( H_1 \), \( H_2 \), \( H_4 \) do modelo de Hubbard |
| **Funções de CVM**           | Parametrização de \(\rho\), entropia de von Neumann, traço parcial, etc. |
| **Minimizador**              | Minimização variacional com LBFGS e penalizações de consistência         |
| **Utilitários**              | Inicialização de parâmetros, verificação de estabilidade, etc.           |

---

## Requisitos

- Python ≥ 3.9  
- Bibliotecas:

## Contato

Para dúvidas ou colaborações, entre em contato:  
lorenzzo.lvsd@usp.br  
lorenzzo.lvsd@gmail.com



## Citação

Se este código for útil para sua pesquisa, por favor cite:

> Delmutti, L. (2025). _Métodos de Variação de Cluster para Férmions na Rede – Fundamentos Matemáticos e Aplicação ao Modelo de Hubbard_. Dissertação de Mestrado, Instituto de Física da Universidade de São Paulo.


```bash
pip install torch numpy matplotlib scipy joblib


