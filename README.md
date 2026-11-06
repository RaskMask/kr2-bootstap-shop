# kr2-bootstrap-shop

## Контрольная работа №2
Тема: «CSS-фреймворки: разработка интерфейса на Bootstrap или альтернативном CSS-фреймворке».

**Студент:** Раскостов Максим Андреевич, группа: ЭФБО-12-25

## Описание проекта
Многостраничный интернет-магазин техники Apple **iStore**, заново собранный на Bootstrap.
Страницы: главная, каталог, карточка товара, форма заказа, контакты.

**Опубликованная версия (GitHub Pages):** https://raskmask.github.io/kr2-bootstrap-shop/

## Используемый фреймворк
Bootstrap 5.3.8.

## Способ подключения
Bootstrap подключён **через CDN** (jsDelivr):
- CSS в `<head>`: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css`;
- собственный `css/custom.css` подключён **после** Bootstrap, чтобы переопределять его стили;
- JS Bundle перед `</body>`: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js`
  (нужен для мобильного меню, модального окна, accordion и tabs).

## Структура проекта
```
kr2-bootstrap-shop/
├── index.html
├── catalog.html
├── product.html
├── order.html
├── contacts.html
├── css/
│   └── custom.css
├── images/
├── README.md
└── .gitignore
```

## Реализованные компоненты Bootstrap
- сетка: `container`, `row`, `col-12 col-md-6 col-lg-4`, `g-3`, `g-4`, `g-5`;
- `navbar` (на всех страницах, сворачивается на мобильных);
- `card`, `btn`, `badge`, `alert` (info и success);
- `modal` (быстрый заказ в каталоге);
- формы: `form-control`, `form-select`, `input-group`, `form-check`;
- `accordion` (частые вопросы на главной);
- `tabs` (характеристики и доставка на странице товара);
- `table`, `list-group`, `ratio` (карта на странице контактов).

## Самостоятельные доработки
- дополнительная страница `contacts.html` с Яндекс.Картой;
- в модальном окне название товара подставляется из кнопки, на которую нажали (`data-product` + событие `show.bs.modal`);
- проверка формы заказа через `.was-validated` и `invalid-feedback`, после отправки показывается `alert-success`;
- тёмная тема через `data-bs-theme="dark"`, цвета и кнопка настроены переопределением переменных Bootstrap в `custom.css`;
- hero-блок с фоновым изображением и затемнением в `custom.css`.

## Как проверить
1. Открыть `index.html` в браузере (или ссылку GitHub Pages).
2. DevTools → режим устройств: проверить перестройку карточек (3 → 2 → 1 колонка) и бургер-меню.
3. Каталог → «Быстрый заказ» → модальное окно открывается и закрывается.
4. Заказ → отправить пустую форму (видны ошибки), затем заполнить (появится зелёный alert).
