---

layout: yandex2

style: |
    /* собственные стили можно писать здесь!! */
    
    .xxx-image { margin: 0 auto;}
    .xxx-image-gr { border: 1px solid #ccc; margin: 30px auto;}
    .xxx-image-adv { width: 100%; }
    .xxx-image-phantom { width: 92%; margin: 60px auto 0; }
    .xxx-shout h2 { font-size: 103px!important;}

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

![](pictures/adv-preview-0.png){:.xxx-image-adv}

## Пример объявления
{:.images}

![](pictures/adv-preview-1.png){:.xxx-image-adv}

## Настройки объявления
{:.fullscreen}

![](pictures/adv-form-0.png){:.xxx-image-gr}

## Пример объявления
{:.images}

![](pictures/adv-preview-1.png){:.xxx-image-adv}

## Пример объявления
{:.images}

![](pictures/adv-preview-2.png){:.xxx-image-adv}

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

![](pictures/phantom-vs-selenium-1.png)

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
    
## Mocha + Selenium
{:.fullscreen}

![](pictures/mocha-selenium-1.png)    
    
## npm i [hermione](https://www.npmjs.com/package/hermione)<br/><br/>npm i [nightwatch](https://www.npmjs.com/package/nightwatch)
{:.shout}    

## Только<br/>интеграционные тесты!
{:.blockquote}

## Отличия модульных и интеграционных тестов
{:.fullscreen}

![](pictures/testing-scheme-1.png)

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/selenium-restrictions-0.png)

## Тесты в headless браузерах
{:.section}

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/headless-0.jpg)

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/phantomjs-scheme-0.png)

## Заголовок будет скрыт
{:.fullscreen}

![](pictures/phantomjs-0.png)

## PhantomJS остановлен
{:.fullscreen}

![](pictures/phantomjs-stop-0.png){:.xxx-image-phantom}

## puppeteer
{:.fullscreen}

![](pictures/puppeteer-0.png)

## Mocha + Selenium
{:.fullscreen}

![](pictures/mocha-puppeteer-1.png)    

## npm i [mocha-headless-chrome](https://www.npmjs.com/package/mocha-headless-chrome)
{:.shout .xxx-shout}

## DEMO
{:.section}

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
- {:.mail}dima117a@yandex-team.ru
- {:.github}dima117

<!-- right -->
- {:.skype}dima117a
- {:.telegram}dima117a

<!-- 
- {:.twitter}@author
- {:.facebook}author

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
