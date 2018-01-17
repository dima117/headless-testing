---

layout: yandex2

style: |
    /* собственные стили можно писать здесь!! */
    
    .xxx-image { margin: 0 auto;}
    .xxx-image-gr { border: 1px solid #ccc; margin: 30px auto;}

---

# ![](themes/yandex2/images/logo-{{ site.presentation.lang }}.svg){:.logo}

## {{ site.presentation.title }}<br />в Headless Chrome
{:.title}

### ![](themes/yandex2/images/title-logo-{{ site.presentation.lang }}.svg){{ site.presentation.service }}

{% if site.presentation.nda %}
![](themes/yandex2/images/title-nda.svg)
{:.nda}
{% endif %}

<div class="authors">
{% if site.author %}
<p>{{ site.author.name }}{% if site.author.position %}{% endif %}</p>
<p>{{ site.author.position }}, Яндекс.Директ</p>
{% endif %}

{% if site.author2 %}
<p>{{ site.author2.name }}{% if site.author2.position %}, {{ site.author2.position }}{% endif %}</p>
{% endif %}

</div>

## О чем поговорим

- {:.next}специфика автотестов веб-интерфейса 
- {:.next}Selenium-тесты <b>vs</b> тесты в headless-браузерах
- {:.next}как скрестить Mocha и headless Chrome

## Почему мы пишем тесты?
{:.section}

## Директ - очень большой проект
{:.fullscreen}

![](pictures/direct-screenshot-0.png){:.xxx-image}

## Пример объявления
{:.images}

![](pictures/adv-preview-0.png){:.xxx-image}

## Пример объявления
{:.images}

![](pictures/adv-preview-1.png){:.xxx-image}

## Настройки объявления
{:.fullscreen}

![](pictures/adv-form-0.png){:.xxx-image-gr}

## Пример объявления
{:.images}

![](pictures/adv-preview-1.png){:.xxx-image}

## Пример объявления
{:.images}

![](pictures/adv-preview-2.png){:.xxx-image}

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/adv-settings-0.png)

## ???
{:.blockquote}

### большой проект, часто меняется, пишем тесты, необохдимый рабочий инструмент

## Тестирование<br />веб-интерфейса
{:.section}

## Тесты для класса/функции

```js
describe('MyClass', () => {
  it('Метод myAction должен возвращать -1', () => {
      // подготовка
      let obj = new MyClass();
      
      // действие
      let result = obj.myAction();
      
      // проверка
      assert.equal(result, -1);
  });
});
```

## Тесты для веб-интерфейса

```js
describe('MyForm', () => {
  it('Должна быть ошибка, если форма не заполнена', () => {
      // подготовка
      let form = createForm();
      
      // действие
      form.submit();
      
      // проверка
      var errorMessage = form.querySelector('.errors');
      assert.equal(errorMessage.innerText, 'Заполните все поля');
  });
});
```

## ???
{:.blockquote}

### браузер - это программа с GUI

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/phantom-vs-selenium.png)

## Selenium-тесты
{:.section}

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/selenium-scheme-0.png)

## Пример Selenium-теста
{:.fullscreen}

```js
describe('Test Suite', function(){

    it('Test Case', function(){

        // подготовка
        browser.url('https://yandex.ru');
        
        // действие
        browser.setValue('#input', 'Я.Субботник');
        browser.submitForm('#search-form');

        // проверка
        expect(browser.getTitle())
            .equals('Я.Субботник - Яндекс: нашлось 52 млн. результатов');
    })
});
```

## Достоинства

![](pictures/selenium-browsers-2.png)
{:.image-right}

- <b>Общий API для всех браузеров<b>

## Достоинства

![](pictures/selenium-grid-0.png)
{:.image-right}

- Общий API для всех браузеров
- <b>Масштабируемость<b>

## Только<br/>интеграционные тесты!
{:.blockquote}

## ???
{:.blockquote}

### Отличия модульных и интеграционных тестов

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/elenium-restrictions-0.png)


## Тесты в headless браузерах
{:.section}

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/headless-0.jpg)

## Как это работает?

![](pictures/headless-scheme.png){:.selenium}

## DEMO!
## Контакты 
{:.contacts}

{% if site.author %}

<figure markdown="1">

### {{ site.author.name }}

{% if site.author.position %}
{{ site.author.position }}
{% endif %}

</figure>

{% endif %}

{% if site.author2 %}

<figure markdown="1">

### {{ site.author2.name }}

{% if site.author2.position %}
{{ site.author2.position }}
{% endif %}

</figure>

{% endif %}

<!-- разделитель контактов -->
-------

<!-- left -->
- {:.skype}author
- {:.mail}author@yandex-team.ru
- {:.github}author

<!-- right -->
- {:.twitter}@author
- {:.facebook}author

<!-- 

- {:.mail}author@yandex-team.ru
- {:.phone}+7-999-888-7766
- {:.github}author
- {:.bitbucket}author
- {:.twitter}@author
- {:.telegram}author
- {:.skype}author
- {:.instagram}author
- {:.facebook}author
- {:.vk}@author
- {:.ok}@author

-->
