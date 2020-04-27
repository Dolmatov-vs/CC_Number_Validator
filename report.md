# Отчёт о тестировании Credit Card Number Validator

## Было проведено тестирование программы проверки валидности номеров банковских карт. В ходе тестирования выявлено, что программа корректно принимает зачения номеров банковских карт длинной в 16 числових символов. Результатом проверки валидных номеров карт maestro с числовой последовательностью 18 символов является FAIL.

С <27.04.2020> по <27.04.2020> было проведено функциональное тестированиет приложения Credit Card Number Validator.

На тестирование затрачено: 2 часа

В результате тестирования выявлены следующие дефекты:
* [Issue 1](https://github.com/Dolmatov-vs/CC_Number_Validator/issues/1)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* [Руководство по установке IntelliJ IDEA](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/idea.md)
* [Программный код указанный в задании 2](https://github.com/netology-code/javaqa-homeworks/tree/master/intro)
* [Образец отчета тестирвования](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/report.md)

В качестве тестовых данных использовались данные фейковых карт Visa, MC, MIR и Maestro взятых с [сайта](https://developer.rbk.money/docs/payments/refs/testcards/):
* Visa 4242424242424242 - Result is OK
* MasterCard 5555555555554444 - Result is OK
* MIR 2201382000000013 - Result is OK
* Данные карты не заполнены - Result is FAIL
* Указан номер карты из одно символа 4 - Result is FAIL
* Номер из 15 символов 491623990046277 - Result is FAIL
* Номер из 17 символов 49162399004627700 - Result is FAIL
* Ввод невалидно номера карты 1234567899876543 -  Result is FAIL
* Ввод символов на латинице "inputlongstrings" - Result is FAIL

Тестирование производилось в следующем окружении:
* Ubuntu 20.04 LTS 64-бит
* IntelliJ IDEA 2020.1 (Community Edition) Build #IC-201.6668.121, built on April 8, 2020
* Runtime version: 11.0.6+8-b765.25 amd64. VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o