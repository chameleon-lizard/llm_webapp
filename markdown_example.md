# Markdown и Math Rendering - Примеры

Этот файл содержит примеры различных элементов Markdown и LaTeX формул для тестирования.

## Текстовое форматирование

**Жирный текст** и *курсив*, а также ***жирный курсив***.

`Inline code` для кода в строке.

~~Зачеркнутый текст~~

## Списки

### Ненумерованный список:
- Первый элемент
- Второй элемент
  - Вложенный элемент
  - Еще один вложенный элемент
- Третий элемент

### Нумерованный список:
1. Первый пункт
2. Второй пункт
3. Третий пункт

## Код

Блок кода на Python:

```python
def factorial(n):
    if n <= 1:
        return 1
    return n * factorial(n - 1)

# Пример использования
result = factorial(5)
print(f"5! = {result}")
```

JavaScript пример:

```javascript
const greet = (name) => {
    console.log(`Hello, ${name}!`);
};

greet("World");
```

## Математические формулы

### Inline формулы

Знаменитая формула Эйнштейна: $E = mc^2$

Теорема Пифагора: $a^2 + b^2 = c^2$

Квадратное уравнение: $x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}$

### Display формулы

Интеграл Гаусса:

$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

Сумма квадратов:

$$
\sum_{i=1}^{n} i^2 = \frac{n(n+1)(2n+1)}{6}
$$

Матрица:

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

Предел:

$$
\lim_{x \to \infty} \frac{1}{x} = 0
$$

Производная:

$$
\frac{d}{dx}(x^n) = nx^{n-1}
$$

Attention механизм (Transformer):

$$
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^\top}{\sqrt{d_k}}\right)V
$$

Формула Байеса:

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

## Таблицы

| Название | Значение | Описание |
|----------|----------|----------|
| Temperature | 0.7 | Контролирует случайность |
| Top P | 0.3 | Nucleus sampling |
| Max Tokens | 2048 | Максимальная длина |

## Цитаты

> Это цитата.
> Она может занимать несколько строк.
>
> И даже иметь несколько параграфов.

## Ссылки

[Документация Markdown](https://www.markdownguide.org/)

[KaTeX Documentation](https://katex.org/)

## Горизонтальная линия

---

## Чекбоксы (GitHub Flavored Markdown)

- [x] Добавить поддержку Markdown
- [x] Добавить поддержку LaTeX формул
- [x] Добавить подсветку синтаксиса
- [ ] Будущие улучшения
