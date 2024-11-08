# Домашнее задание по теме "Систематизация и пропуск тестов".

Цель: понять на практике как объединять тесты при помощи ```TestSuite```.
Научиться пропускать тесты при помощи встроенных в ```unittest``` декораторов.

Задача "Заморозка кейсов":

Подготовка:

В этом задании используйте те же ```TestCase```, что и в предыдущем:
```RunnerTest``` и ```TournamentTest```.

Часть 1. ```TestSuit```.

1. Создайте модуль suite_12_3.py для описания объекта ```TestSuite```.
   Укажите на него переменной с произвольным названием.
2. Добавьте тесты ```RunnerTest``` и ```TournamentTest``` в этот
   ```TestSuit```.
3. Создайте объект класса ```TextTestRunner```, с аргументом ```verbosity=2```.

Часть 2. Пропуск тестов.

1. Классы ```RunnerTest``` дополнить атрибутом ```is_frozen = False``` и
   ```TournamentTest``` атрибутом ```is_frozen = True```.
2. Напишите соответствующий декоратор к каждому методу (кроме
   ```@classmethod```), который при значении ```is_frozen = False``` будет
   выполнять тесты, а ```is_frozen = True``` - пропускать и выводить
   сообщение ```'Тесты в этом кейсе заморожены'```.

Таким образом вы сможете контролировать пропуск всех тестов в ```TestCase```
изменением всего одного атрибута.
Запустите ```TestSuite``` и проверьте полученные результаты тестов из обоих
```TestCase```.

Пример результата выполнения тестов:

Вывод на консоль:
```
test_challenge (tests_12_3.RunnerTest.test_challenge) ... ok
test_run (tests_12_3.RunnerTest.test_run) ... ok
test_walk (tests_12_3.RunnerTest.test_walk) ... ok
test_first_tournament (tests_12_3.TournamentTest.test_first_tournament) ... skipped 'Тесты в этом кейсе заморожены'
test_second_tournament (tests_12_3.TournamentTest.test_second_tournament) ... skipped 'Тесты в этом кейсе заморожены'
test_third_tournament (tests_12_3.TournamentTest.test_third_tournament) ... skipped 'Тесты в этом кейсе заморожены'
----------------------------------------------------------------------
Ran 6 tests in 0.000s OK (skipped=3)
```

Файлы suite_12_3.py и tests_12_3.py, где произошли изменения загрузите на
ваш GitHub репозиторий. В решении пришлите ссылку на него.

Успехов!
