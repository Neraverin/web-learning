# Полезные снипетты при работе с Emmet
## Общий пример
Конструкция вида:
``#page>div.logo+ul#navigation>li*5>a{Item $}`` разворачиваается в 
```html
<div id="page">
    <div class="logo"></div>
        <ul id="navigation">
        <li><a href="">Item 1</a></li>
        <li><a href="">Item 2</a></li>
        <li><a href="">Item 3</a></li>
        <li><a href="">Item 4</a></li>
        <li><a href="">Item 5</a></li>
    </ul>
</div>
```
## Популярные сниппеты
- tag1+tag2 = два тега последовательно
- tag1>tag2 = tag2 будет вложен внутрь tag1
- tag1^tag2 = tag2 будет поставлен на уровне выше, чем tag1 (можно использовать больше 1 раза, то есть '^^')
- tag1*n = повторение tag1 n-раз подряд (очень удобно для списков)
- tag1#id1 = создание тега tag1 с id = id1
- tag1.class1 = создание тега tag1 с классом class1 (может использоваться больше 1 раза, то есть '.class1.class2')
- $ - символ используется для аавтоматической подстановки последоваательных значений (см. общий пример выше)
- table>.row>.cell будет автоматически заменен на:
```html
        <table>
            <tr class="element">
                <td class="cell"></td>
            </tr>
        </table>
```