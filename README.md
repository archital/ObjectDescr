# ObjectDescr

Обьект: Клиент
1) Атрибуты: Фамилия, Имя, Отчество, Серия_Номер_Паспорта, список счетов в банке.
2) Методы: добавитьКлиентаВБД, удалитьКлиентасБД, записатьФамилиюПоПаспортнымДанным, податьЗаявкуНаОткрытиеСчета. 
3) Иерархия: 
    Предки: 
        юрЛицо
    Потомки:
        - Заемщик
    	- Депозитор 
		юрЛицо -> человек
4) Интерфейс: 
    юрЛицо: 
        записатьФамилиюПоПаспортнымДанным()
        податьЗаявкуНаОткрытиеСчета()
5) Полиморфное поведение методов:
      записатьФамилиюПоПаспортнымДанным(): 
         изменитьФамилиюВбд()
      податьЗаявкуНаОткрытиеСчета():
         открытьСчет()
6) Спрятанные методы:
    изменитьФамилиюВбд()
    податьЗаявкуНаОткрытиеСчета()
    Спрятанное поле:
        наличие_счета
7) Клиент может быть Сотрудником Банка.
Сотрудниками Банка могут быть один или много клиентов.

Объект: Человек
    Реализует интерфейс юрЛицо
        изменитьФамилиюВбд():
            изменитьфамилиюВпаспортномСтоле(): спрятанный метод
         открытьСчет():
         податьДокументыНаОткрытиеСчета(): спрятанный метод
