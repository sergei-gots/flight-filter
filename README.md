# flight-filter

## Авиаперелеты
<br>Задача
<br><br>
Имеется некая система, которая обрабатывает авиаперелёты. Перелёт — это перевозка пассажира из одной точки в другую с возможными промежуточными посадками. Т. о. перелёт можно представить как набор из одного или нескольких элементарных перемещений, называемых сегментами. <br><br>
<b>Сегмент</b> — это атомарная перевозка, которую для простоты будем характеризовать всего двумя атрибутами: <br><li>дата/время вылета <li>дата/время прилёта.
<br>
<br>
Следует написать небольшой модуль, который будет заниматься фильтрацией набора перелётов согласно различным правилам. Правил фильтрации может быть очень много. Также наборы перелётов могут быть очень большими. Правила могут выбираться и задаваться динамически в зависимости от контекста выполнения операции фильтрации.
<br>
<br>
Необходимо продумать структуру модуля, создать необходимые классы и интерфейсы. Хорошо, если код покрыт тестами JUnit. 
<br>Пользовательский интерфейс не рассматривается. Достаточно вывода информации в консоль. Никаких сторонних библиотек использовать не нужно.
<br><br>
Приложенный файл TestClasses.java содержит упрощённые модельные классы и фабрику для получения тестовых образцов. Весь код необходимо поместить в пакет com.gridnine.testing
<br><br>
Для проверочного запуска должен быть создан публичный класс Main c методом main() Этот метод должен выдать в консоль результаты обработки тестового набора перелётов. Получить тестовый набор нужно методом FlightBuilder.createFlights()
<br><br>
В main() следует поместить такой проверочный код. Исключите из тестового набора перелёты по следующим правилам (по каждому правилу нужен отдельный вывод списка перелётов):
<br><br>
<li>вылет до текущего момента времени
<li>имеются сегменты с датой прилёта раньше даты вылета
<li>общее время, проведённое на земле превышает два часа (время на земле — это интервал между прилётом одного сегмента и вылетом следующего за ним)
