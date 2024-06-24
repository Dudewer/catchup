# Цель
Добавить оценку времени для оставшегося до окончания выполнения catchup
# Описание
В catchup_send_recieve_handler.go было необходимо добавить отслеживание времени начала выполнения, добавить функцию для оценки оставшегося времени, вывод или логирование оценки оставшегося время.
Было решено изменить функции HandleCatchupSend и HandleCatchupReceive. 
# Результат
Был модифицирован catchup_send_recieve_handler.go
Вычисляется общее количество файлов и общий размер по списку файлов.
Увеличивается количество обработанных файлов и их размер по мере выполнения каждой команды.
Рассчитывается среднее время работы над файлом, используя затраченное время и количество обработанных файлов.
Оценивается оставшееся время на основе количества оставшихся файлов и среднего времени работы над файлом.
Логируется оставшееся время в течение каждой итерации.

