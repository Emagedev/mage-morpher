# API сайта morpher.ru для Magento 1.9
Этот модуль позволит склонять слова в зависимости от контекста с помощью онлайн
сервиса morpher.ru. Первый запрос осуществляется через REST API, дальнейшие - из
кэша в базе данных, что позволяет не нагружать сервис лишними запросами (они ограничены
по бесплатной и платной подпискам). 

### Использование с числами
Модуль поможет склонять слова рядом с числами, например, для количества товаров в каталоге или корзине.

Так, вызов хелпера со следующими параметрами

```Mage::helper('emagedev_russian')->inflectWordByNumber(5, 'товар', true);```

Вернет
> 5 товаров

### Склонение имён
Полезной возможностью является склонение имён пользователей бла-бла

### Авторизация на morpher.ru
Для авторизации на сайте - она необходима

---

> **N.B. Не забывайте модифицировать ключи кэша для корректной работы с числами.**

> **N.B. Так как функции модуля - косметические, модуль _как правило_ не поднимает ошибок. Если что-то работает некорректно, стоит посмотреть в логи.**