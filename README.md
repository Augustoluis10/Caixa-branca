# 🧪 Análise de Caixa Branca – Método `verificarUsuario`

Este repositório contém a análise estrutural do método `verificarUsuario()` utilizando **técnicas de Caixa Branca**, incluindo:

- Construção do grafo de fluxo de controle  
- Cálculo da complexidade ciclomática  
- Identificação dos caminhos básicos  
- Exemplos de validação / invalidação  
- Tabela resumo da análise

---

## 📌 Estrutura do Grafo (Nós)

O grafo do método contém os seguintes nós:

1. **N1** – Início  
2. **N2** – Declaração / inicialização da variável `sql`  
3. **N3** – Chamada `conectarBD()`  
4. **N4** – Montagem da instrução SQL  
5. **N5** – Criação do Statement / execução da query  
6. **N6** – Decisão `rs.next()`  
7. **N7** – Caminho quando existe resultado → `result = true`  
8. **N8** – Atribuição de `nome = rs.getString("nome")`  
9. **N9** – Caminho quando não existe resultado → `result = false`  
10. **N10** – Retorno final (`return result`)

---

## 🔢 Cálculo da Complexidade Ciclomática

A fórmula usada foi:

```
M = E - N + 2P
```

Onde:

- **E** = número de arestas = 10  
- **N** = número de nós = 10  
- **P** = componentes conectados = 1  

### ✔️ Resultado

```
M = 10 - 10 + 2(1) = 2
