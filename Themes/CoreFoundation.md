CoreFoundation
==

###1 Question:

True or False? You should use NSHost when connecting to a specific host.

* False (You should use CFHost)
* True


##2 Question:


What kind of socket does a CFSocket use?

* A BSD Socket
* A NSOperationsQueue socket
* A TCP/IP socket


BSD Socket - сокеты Беркли (API сокетов BSD)
Обмен данными с использованием протокола TCP. 
Лиценция BSD - Berkeley Software Distribution.

http://zed.karelia.ru/go.to/for.students/computer.networks/bsd.sockets
https://ru.wikipedia.org/wiki/Сокеты_Беркли

В  протоколах TCP/IP в сетевом порядке байтов хранятся, в частности, IP-адрес и номер TCP-порта.

Разработка сервера

Основные действия, которые должна выполнить программа-сервер:

1. Cоздать сокет (программное гнездо)
2. Дать сокету имя (адрес)
3. Объявить сокет могущим принимать соединения
4. Принять соединение
5. По окончании работы закрыть сокет