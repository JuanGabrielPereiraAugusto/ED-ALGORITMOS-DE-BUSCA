# 🔍 Estrutura de Dados — Algoritmos de Busca

Trabalho acadêmico da disciplina de **Estrutura de Dados** na **Fatec Taquaritinga**, com 4 questões resolvidas sobre **algoritmos**, **busca linear**, **Merge Sort** e **busca em árvore binária**.

📄 **Trabalho completo:** [`Trabalho_ED_Algoritmos_de_Busca.docx`](Trabalho_ED_Algoritmos_de_Busca.docx)

---

## 📋 Questões

| # | Tema | Resposta |
|---|---|---|
| 1 | 🧩 O que é um algoritmo | Questão dissertativa |
| 2 | ➡️ Busca linear | **c)** percorre os elementos um a um até encontrar o valor |
| 3 | ✂️ Algoritmo que divide o vetor | **c)** Merge Sort |
| 4 | 🌳 Busca em árvore binária | **2)** 50 – 70 – 60 |

---

## 1️⃣ O que é um algoritmo

Uma **sequência finita, ordenada e bem definida de passos** que, a partir de dados de entrada, resolve um problema e produz um resultado.

| Característica | Significado |
|---|---|
| **Finitude** | Termina depois de um número finito de passos |
| **Definição** | Cada instrução é precisa, sem ambiguidade |
| **Entrada** | Recebe zero ou mais dados |
| **Saída** | Produz pelo menos um resultado |
| **Efetividade** | Cada passo pode ser feito em tempo finito |

**No cotidiano:** uma receita de bolo. Os ingredientes são a entrada, o modo de preparo são os passos e o bolo pronto é a saída.

---

## 2️⃣ Busca linear

✅ **Resposta: c)** percorre os elementos um a um até encontrar o valor.

A busca compara o valor com cada elemento, do primeiro ao último. No pior caso, olha todos os **n** elementos, ou seja, **O(n)**.

| Alternativa | Por que está errada |
|---|---|
| a) só funciona com dados ordenados | Funciona com dados ordenados ou não; quem exige ordenação é a busca binária |
| b) sempre O(log n) | É O(n); O(log n) é a busca binária |
| d) usa árvore binária | Funciona em vetores e listas comuns |

```csharp
static int BuscaLinear(int[] vetor, int valor)
{
    for (int i = 0; i < vetor.Length; i++)
    {
        if (vetor[i] == valor)
            return i;     // encontrou: retorna a posição
    }
    return -1;            // não encontrou
}
```

---

## 3️⃣ Algoritmo que divide o vetor em partes menores

✅ **Resposta: c) Merge Sort.**

Usa **divisão e conquista**: divide o vetor ao meio até sobrar um elemento em cada parte e depois junta (*merge*) as partes em ordem. A complexidade é **O(n log n)**.

```
Divisão:      [38, 27, 43, 3] → [38, 27] [43, 3] → [38] [27] [43] [3]
Intercalação: [27, 38] [3, 43] → [3, 27, 38, 43]
```

Bubble Sort, Selection Sort e Insertion Sort **não dividem** o vetor: comparam e trocam elementos no vetor inteiro, com complexidade **O(n²)** no pior caso.

---

## 4️⃣ Busca em árvore binária

✅ **Resposta: 2) 50 – 70 – 60.**

```
      50
     /  \
   30    70
        /
      60
```

Na árvore binária de busca, os **menores ficam à esquerda** e os **maiores à direita**:

| Passo | Nó | Decisão |
|---|---|---|
| 1 | 50 | 60 > 50 → vai para a **direita** |
| 2 | 70 | 60 < 70 → vai para a **esquerda** |
| 3 | 60 | ✅ Encontrado |

O nó 30 nunca é visitado, porque só seria visitado na busca de valores menores que 50.

---

## 🎓 Informações acadêmicas

| | |
|---|---|
| **Instituição** | Fatec Taquaritinga |
| **Curso** | Análise e Desenvolvimento de Sistemas — 3º semestre |
| **Disciplina** | Estrutura de Dados |
| **Professora** | Gislaine Cristina da Conceição |
| **Ano** | 2026 |

## 👥 Integrantes

- Juan Gabriel Pereira Augusto
- Vitor Gomes de Oliveira
