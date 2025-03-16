

# Gilded Rose Refactoring Kata

## Descrição

Este repositório contém a solução para o exercício **Gilded Rose Refactoring Kata**, incluindo a implementação de testes unitários e a refatoração do código para atender às especificações de requisitos.

O código inicial pode ser encontrado no repositório original: [GildedRose-Refactoring-Kata](https://github.com/emilybache/GildedRose-Refactoring-Kata)

## Objetivo

- Implementar testes unitários para garantir o correto funcionamento do sistema.
- Identificar e corrigir "code smells" no código original.
- Refatorar a lógica do sistema mantendo a compatibilidade com os requisitos originais.
- Adicionar suporte para uma nova categoria de itens.

## Requisitos

O sistema de gerenciamento de estoque da Gilded Rose segue as seguintes regras:

- Todos os itens possuem:
  - `sellIn`: número de dias para venda.
  - `quality`: valor que representa a qualidade do item.
- No final do dia, os valores de `sellIn` e `quality` de cada item são atualizados conforme as regras:
  - A qualidade diminui a cada dia.
  - Após a data de venda (`sellIn <= 0`), a qualidade diminui duas vezes mais rápido.
  - A qualidade nunca pode ser negativa.
  - O item "Aged Brie" aumenta de qualidade com o tempo.
  - A qualidade máxima permitida para um item é 50.
  - "Sulfuras" é um item lendário e não sofre alterações.
  - "Backstage Passes" aumentam de qualidade conforme o evento se aproxima:
    - +2 se `sellIn` <= 10.
    - +3 se `sellIn` <= 5.
    - Qualidade cai para 0 após o evento.
  - "Conjured" degradam duas vezes mais rápido.

## Entrega

Juntamente ao código fonte, deve ser entregue um relato contendo:

1. Estratégia adotada para a criação dos testes.
2. "Code smells" identificados no código original.
3. Refatorações aplicadas e justificativa.
4. Dificuldades encontradas.
5. Lições aprendidas.

Alternativamente, pode-se gravar um vídeo documentando o processo de refatoração e enviar como entrega.

## Como executar os testes

Para rodar os testes unitários, utilize:

```sh
python -m unittest discover

