# Тест формул

## Формула Attention из вашего примера

Вычисление внимания между запросами (queries), ключами (keys) и значениями (values):

$$
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^\top}{\sqrt{d_k}}\right)V
$$

где:
- $Q$ — матрица запросов размера $n \times d_k$,
- $K$ — матрица ключей размера $m \times d_k$,
- $V$ — матрица значений размера $m \times d_v$,
- $d_k$ — размерность ключей и запросов,
- $n$ — количество запросов,
- $m$ — количество ключей/значений.

## Дополнительные тесты

Multi-head attention:

$$
\text{MultiHead}(Q, K, V) = \text{Concat}(\text{head}_1, \ldots, \text{head}_h)W^O
$$

где каждая голова вычисляется как:

$$
\text{head}_i = \text{Attention}(QW_i^Q, KW_i^K, VW_i^V)
$$

## Inline формулы

Формула Эйнштейна $E = mc^2$ и квадратный корень $\sqrt{2}$ в тексте.

Также греческие буквы: $\alpha$, $\beta$, $\gamma$, $\delta$, $\epsilon$, $\theta$, $\lambda$, $\mu$, $\pi$, $\sigma$, $\omega$.
