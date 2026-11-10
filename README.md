# 🛒 Sistema de Cadastro e Controle de Estoque (Sacolão)

Este é um projeto em Python desenvolvido para gerenciar o inventário de produtos e seus respectivos preços de forma simples e interativa via console.

## 🚀 Funcionalidades

- **Visualização de Estoque:** Exibição clara e organizada de todos os produtos cadastrados e seus respectivos preços formatados em Real (R$).
- **Cadastro Dinâmico:** Permite a inserção de novos itens e preços no estoque em tempo real.
- **Exclusão Inteligente:** Sistema para remover produtos indesejados mantendo a integridade e sincronização entre as listas de nomes e valores.

## 🛠️ Tecnologias Utilizadas

- **Python 3**
- **Estruturas de Dados:** Listas emparelhadas (`list`)
- **Iteradores e Funções Nativas:** `zip()`, `pop()`, `append()`, `range()` e `len()`

## 📋 Como Funciona o Código

O sistema utiliza duas listas paralelas para sincronizar o nome do item e seu valor:
```python
lista1 = ["Camisa Basica", "Calça Jeans", "Jaqueta de couro"]
lista2 = [49.90, 129.90, 219.90]
```

A manipulação dos índices garante que ao adicionar ou remover um item de uma lista, a outra seja atualizada na mesma proporção:

* **Para Adicionar:**
  ```python
  lista1.append(novo_produto)
  lista2.append(novo_preco)
  ```
* **Para Remover:**
  ```python
  # Encontra a posição exata e remove de ambas de forma síncrona
  indice = lista1.index(produto_excluir)
  lista1.pop(indice)
  lista2.pop(indice)
  ```

## 👤 Autor

Desenvolvido por Murilo durante a jornada de aprendizado em lógica de programação com Python na Generation Brasil.
