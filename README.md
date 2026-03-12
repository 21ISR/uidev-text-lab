# Применение CSS свойств текста

## Цель:

Используя только CSS (_просьба не менять теги, однако добавлять классы и айди можно_), оформить готовую HTML-страницу так, чтобы все элементы корректно отображались согласно референсу

_Понимаю, что пиксель перфект без референсов значений будет сделать сложно, поэтому просто постарайтесь повторить как можно ближе к референсу_

### Шрифты

Шрифты необходимо подключать через HTML теги с сервиса [Google Fonts](https://fonts.google.com)

_Скажем кое-кому спасибо за доступ к Гугл Шрифтам, поэтому вот тэги_

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
```


#### Шрифты используемые в задании

- Montserrat
- Roboto
- Playfair Display

## Готовый макет

<img src="./.repo/finished.jpg?" />

## Подсказка

## Шрифт и размер

| Свойство | Что делает | Пример |
|---|---|---|
| `font-family` | Задаёт шрифт | `font-family: 'Arial', sans-serif;` |
| `font-size` | Размер текста | `font-size: 16px;` |
| `font-weight` | Жирность текста | `font-weight: bold;` или `font-weight: 700;` |
| `font-style` | Курсив | `font-style: italic;` |

```css
/* Пример: заголовок блога */
h1 {
  font-family: 'Georgia', serif;
  font-size: 32px;
  font-weight: bold;
}

/* Пример: курсивный подзаголовок */
h3 {
  font-style: italic;
}
```

---

## Подключение шрифтов с Google Fonts

Google Fonts — бесплатный сервис с сотнями шрифтов. Подключается в два шага.

**Шаг 1.** Вставь тег `<link>` в `<head>` HTML-файла **до** подключения CSS:

```html
<head>
  <!-- ... -->
  <!-- Подключение шрифта с Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">

  <!-- CSS — всегда после шрифтов -->
  <link rel="stylesheet" href="style.css">
</head>
```

**Шаг 2.** Используй шрифт в CSS через `font-family`:

```css
body {
  font-family: 'Roboto', sans-serif;
}
```

**Запасной шрифт (fallback)** — всегда указывай через запятую на случай, если шрифт не загрузится:

```css
font-family: 'Roboto', Arial, sans-serif;
/* Браузер попробует Roboto → Arial → любой sans-serif */
```

---

## Цвет и выделение

| Свойство | Что делает | Пример |
|---|---|---|
| `color` | Цвет текста | `color: #333;` |
| `background-color` | Фон под текстом (выделение) | `background-color: yellow;` |

```css
/* Пример: выделение слова как маркером */
.highlight {
  background-color: yellow;
  color: #000;
}

/* Пример: ссылка синего цвета */
a {
  color: #1a73e8;
}
```

---

## Оформление и трансформация

| Свойство | Что делает | Значения |
|---|---|---|
| `text-decoration` | Подчёркивание, зачёркивание | `underline` / `line-through` / `none` |
| `text-transform` | Регистр букв | `uppercase` / `lowercase` / `capitalize` |
| `letter-spacing` | Расстояние между буквами | `letter-spacing: 4px;` |

```css
/* Пример: зачёркнутый текст */
.strikethrough {
  text-decoration: line-through;
}

/* Пример: текст в верхнем регистре */
.uppercase {
  text-transform: uppercase;
}

/* Пример: разрядка букв */
.spaced {
  letter-spacing: 6px;
}
```

---

## Выравнивание и межстрочный интервал

| Свойство | Что делает | Значения |
|---|---|---|
| `text-align` | Выравнивание по горизонтали | `left` / `center` / `right` / `justify` |
| `line-height` | Высота строки | `line-height: 1.6;` |
| `text-indent` | Отступ первой строки абзаца | `text-indent: 40px;` |

```css
/* Пример: заголовок по центру */
h1 {
  text-align: center;
}

/* Пример: удобочитаемый основной текст */
p {
  text-align: justify;
  line-height: 1.8;
}

/* Пример: красная строка как в книге */
p {
  text-indent: 40px;
}
```

# Как сдавать

- Создайте форк репозитория в вашей организации с названием-этого-репозитория-вашафамилия
- Используя ветку wip сделайте задание
- Зафиксируйте изменения в вашем репозитории
- Когда документ будет готов - создайте пул реквест из ветки wip (вашей) на ветку main (тоже вашу) и укажите меня (ktkv419) как reviewer

Не мержите сами коммит, это сделаю я после проверки задания
