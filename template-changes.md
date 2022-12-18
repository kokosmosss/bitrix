# Изменения в шаблон

### Изменить в хэдере кнопки логина-регистрации
Необходимо удалить из разметки иконку, так как в дизайн-макете ее нет.  
Кнопка должна выглядеть так (дата-атрибуты, необходимые для работы js опущены):
```html
<a class="header-cabinet__link fill-theme-hover light-opacity-hover dark_link animate-load" href="#">
  Войти
</a>
```
Кнопка регистрации должна идти после кнопки логина.

### Удалить картинку со слайда swiper
Необходимо удалить фоновую картинку сплошного белого цвета, которая указана для первого (и единственного) слайда swiper.  
Если это невозможно, то можно воспользоваться [полностью прозрачным изображением](./source/img/transparent.png).

## Классы и теги для стилизации специфических блоков

### Добавить класс в промо-блок "Выбирай добро"
Необходимо добавить класс `custom-banner` для стилизации промо-блока
Было:
```html
<div class="drag-block container BIG_BANNER_INDEX" data-class="big_banner_index_drag" data-order="1">
  ...
</div>
```

Станет:
```html
<div class="drag-block container BIG_BANNER_INDEX custom-banner" data-class="big_banner_index_drag" data-order="1">
  ...
</div>
```

### Добавить класс в блок с карточками под промо-блоком
Необходимо добавить класс `custom-cards` для стилизации карточек
Было:
```html
<div class="banners-img-with-text-list banners-with-text-template">
  ...
</div>
```

Станет:
```html
<div class="banners-img-with-text-list banners-with-text-template custom-cards">
  ...
</div>
```

### Добавить класс в блок "Наши достижения"
Необходимо добавить класс `custom-achievements` для стилизации блока "Наши достижения"
Было:
```html
<div class="drag-block container TIZERS " data-class="tizers_drag" data-order="5">
  ...
</div>
```

Станет:
```html
<div class="drag-block container TIZERS custom-achievements" data-class="tizers_drag" data-order="5">
  ...
</div>
```

### Добавить классы и теги в блок "С заботой о природе"
Нужно переместить заголовок "С заботой о природе" внутрь центровщика следующего за ним блока.  
Так же нужно добавить класс `custom-nature` на общую обертку.

Было:
```html
<h2>C заботой о природе</h2>
<div class="tizers-list  tizers-list--narrow">
  <div class="maxwidth-theme">
    ...
  </div>
</div>
```

Станет:
```html
<div class="tizers-list tizers-list--narrow custom-nature">
  <div class="maxwidth-theme">
    <h2>C заботой о природе</h2>
    ...
  </div>
</div>
```

Добавить кнопку в конец блока `<div class="maxwidth-theme">`

```html
<div class="index-block__btn">
  <a href="/#" class="button-link button-link--white">
    Узнай больше об эко-привычках с KFC
  </a>
</div>
```

### Добавить классы и теги в блок "Волонтерство"
Необходимо добавить класс `custom-volunteering` для стилизации блока
Было:
```html
<div class="company-item front_company-template">
  ...
</div>
```

Станет:
```html
<div class="company-item front_company-template custom-volunteering">
  ...
</div>
```

Необходимо для списка с итогами добавить общую обертку и удалить лишние переносы строк (один `<br>` в конце и по одному в каждом из 4-х пунктов).  
Было:
```html
<div class="main-item">
  <b>3000</b><br>
  волонтеров
</div>
<div class="main-item">
  <b>300</b><br>
  добрых проектов
</div>
<div class="main-item">
  <b>10 000</b><br>
  благополучателей
</div>
<div class="main-item">
  <b>10 000</b><br>
  благотворительных обедов
</div>
<br>
```

Станет:
```html
<div class="main-item-container">
  <div class="main-item">
    <b>3000</b>
    волонтеров
  </div>
  <div class="main-item">
    <b>300</b>
    добрых проектов
  </div>
  <div class="main-item">
    <b>10 000</b>
    благополучателей
  </div>
  <div class="main-item">
    <b>10 000</b>
    благотворительных обедов
  </div>
</div>
```

Необходимо изменить классы для кнопки регистрации, так как она в макете выглядит как ссылка.    
Было:
```html
<a href="/#" class="btn btn-transparent-border btn-lg">
  Зарегистрируйся на событие
</a>
```
Станет:
```html
<a href="/#" class="button-link">
  Зарегистрируйся на событие
</a>
```

И добавить новую кнопку в конец блока `<div class="company-item front_company-template">`:
```html
<div class="index-block__btn index-block__btn--subscribe">
  <a href="/#" class="btn btn-default">
    Подпишись на рассылку
  </a>
</div>
```

### Добавить классы в блок "Благотворительность"
Необходимо добавить класс `custom-charity` для стилизации блока
Было:
```html
<div class="company-item front_company-template">
  ...
</div>
```

Станет:
```html
<div class="company-item front_company-template custom-charity">
  ...
</div>
```

В параграфе необходимо выделить тегом `<b>` часть текста.  
Было:
```html
<p>
  Работа с подопечными фонда «Открывая горизонты» — одно из ключевых направлений волонтерской помощи KFC. Это помощь подросткам из детских домов в социализации и профориентации в таком важном периоде, как подготовка к будущей самостоятельной жизни. Поддержать работу фонда легко — через онлайн пожертвование по кнопке ниже. А чтобы стать волонтером фонда, заполни анкету на на сайте&nbsp;«Открывая горизонты».
</p>
```
Станет:
```html
<p>
  Работа с подопечными фонда «Открывая горизонты» — одно из ключевых направлений волонтерской помощи KFC. Это помощь подросткам из детских домов в социализации и профориентации в таком важном периоде, как подготовка к будущей самостоятельной жизни. <b>Поддержать работу фонда легко — через онлайн пожертвование по кнопке ниже.</b> А чтобы стать волонтером фонда, заполни анкету на на сайте&nbsp;«Открывая горизонты».
</p>
```

Добавить в конец блока `<div class="sticky-block flexbox--mb20-t991">` код с двумя кнопками вместо одной:  
Было:
```html
<div class="index-block__btn">
  <a href="/#" class="btn btn-transparent-border btn-lg">
    Узнать больше не сайте фонда
  </a>
</div>
```

Станет:
```html
<div class="index-block__btn-wrapper">
  <div class="index-block__btn">
    <a href="/#" class="button-link">
      Сделать пожертвование
    </a>
  </div>

  <div class="index-block__btn">
    <a href="/#" class="button-link">
      Узнать больше на сайте фонда
    </a>
  </div>
</div>
```

Добавить в конец блока `<div class="company-item front_company-template">` новую кнопку:
```html
<div class="index-block__btn index-block__btn--subscribe">
  <a href="/#" class="btn btn-default">
    Подпишись на рассылку
  </a>
</div>
```
