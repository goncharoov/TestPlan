# План автоматизации тестирования записи на обучение профессии "Тестировщик ПО"

## Предусловия:
Переход к форме заполнения заявки на сайте https://netology.ru с главной страницы осуществляется несколькими способами:

### Способ 1

1. Зайти на страницу 
2. Кликнуть на выпадающее меню "Каталог курсов", в разделе "Программирование" выбрать "Тестировщик ПО" 
3. Перейти к форме записи по клику на кпонку "Записаться" в блоке "Профессия" или пролистать страницу до блока "Запишитесь или получите консультацию"

### Способ 2

1. Зайти на страницу 
2. Кликнуть на выпадающее меню "Каталог курсов", выбрать пункт "Полный каталог"
3. Выбрать в списке профессию "Тестировщик ПО"
3. Перейти к форме записи по клику на кпонку "Записаться" в блоке "Профессия" или пролистать страницу до блока "Запишитесь или получите консультацию"

### Способ 3

1. Зайти на страницу 
2. Кликнуть на "НЕО для начинающих"
3. В списке профессий выбрать "Тестировщик ПО" 
4. Перейти к форме записи по клику на кпонку "Записаться" в блоке "Профессия" или пролистать страницу до блока "Запишитесь или получите консультацию"

### Форматы данных для полей

1. Поле "Имя" принимает только кириллицу или латинницу. Пользователь может ввести ФИО целиком или только имя. Ограничение поля 64 символа.
2. Поле "Телефон" принимает только цифры. Номер должен содержать 11 цифр и начинаться на +7 

## Тестовые сценарии

**Сценарий 1. Отправка формы с валидными данными** 

1. Ввести в поле "Имя" валидные данные. Например: Иван 
2. Ввести в поле "Телефон" валидный номер мобильного. Например: +79123456789
3. Нажать кнопку "Записаться"

***Ожидаемый резульат:*** форма отправляется, пользователю открывается уведомление об успешной записи

**Сценарий 2. Отправка пустой формы**

1. Поле "Имя" оставить пустым
2. Поле "Телефон" оставить пустым
3. Нажать кнопку "Записаться"

***Ожидаемый резульат:*** форма не отправляется, пользователю открывается уведомление об обязательном заполнении полей.

**Сценарий 3. Отправка формы с невалидным именем**

1. Ввести в поле "Имя" невалидные данные. Например: набор цифр
2. Ввести в поле "Телефон" валидный мобильный номер
3. Нажать кнопку "Записаться"

***Ожидаемый резульат:*** форма не отправляется, пользователю открывается уведомление о том что поле заполнено неверно.

**Сценарий 4. Отправка формы с невалидным телефоном**

1. Ввести в поле "Имя" валидные данные
2. Ввести в поле "Телефон" невалидные данные. Например: менее 11 цифр
3. Нажать кнопку "Записаться"

***Ожидаемый резульат:*** форма не отправляется, пользователю открывается уведомление о том что поле заполнено неверно.

## Перечень используемых инструментов с обоснованием выбора

**Java 11**

Универсальный язык программирования для создания автотестов с использованием наиболее популярных фреймворков и необходимых библиотек

**IntelliJ IDE**

Бесплатная среда разработки, имеющая большой функционал для создания тестов на Java

**JUnit 5**

Платформа для создания юнит-тестов на Java

**Selenide**

Фрейворк для автоматизированного тестирования UI

**Git**

Система контроля версий для управления измениями в коде и их систематизация в одном репозитории 

**AppVeyor**

CI/CD сервис для проверки и тестирования сборки проекта при каждом изменении версии в репозитории

## Перечень необходимых разрешений/данных/доступов от банка 

* Разрешение на проведене тестирования сайта

* Резрешение на автоматизацию тестирования

## Перечень и описание возможных рисков при автоматизации

* Стоимость автоматизированного тестирования, тк никто не может гарантировать написание правильных тестов в короткие сроки. Что по сути может занять время на проверку самих тестов
* Поиск нужных локаторов для создания автотестов может занять большое количество времени, по сравнению с ручным тестированием формы
* Не своевременная поддержка тестов может повлечь их "поломку"


## Перечень необходимых специалистов для автоматизации

* Специалист по автоматизации 

## Интервальная оценка с учётом рисков (в часах)

* Время на разработку тестов 3-5 часов
* Запас времени 5 часов

