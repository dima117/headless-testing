---

layout: yandex2

style: |
    /* собственные стили можно писать здесь!! */
    
    .xxx-image { margin: 30px auto;}
    .xxx-image-gr { border: 1px solid #ccc; margin: 30px auto;}
    .selenium { width: 1200px; margin: 0 auto;}
    .adv-direct { width: 1000px; margin: 0 auto;}
    .adv-preview2 { width: 1200px; margin: 0 auto;}
    .headless { width: 1000px; margin: 0 auto;}    
    
    

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

![](pictures/adv-settings.png)

## Selenium-тесты
{:.section}

## Как это работает?

![](pictures/selenium.png){:.selenium}

## Достоинства

- одинаковый API для разных браузеров
- масштабируемость

## Только интеграционные тесты!
{:.blockquote}

## Отличия тестов

- модульные тесты изолируют зависимости
- интеграционные тесты проверяют всё вместе

## Как это работает?

![](pictures/selenium.png){:.selenium}

## Исходный код (js)

Пояснение для кода.

```js
describe('Test Suite', function(){

    it('Test Case', function(){

        // navigate to a new URL
        browser.url('https://yandex.ru');
        browser.setValue('#input', 'Я.Субботник');
        browser.submitForm('#search-form');

        var title = browser.getTitle();
        expect(title).equals('Я.Субботник - Яндекс: нашлось 52 млн. результатов');
    })
});
```

## Тесты в headless браузерах
{:.section}

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/headless.jpg){:.headless}

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
