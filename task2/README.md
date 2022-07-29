# Задание №2

В данном задании вы закрепите типы данных, ветвления и циклы, решите несколько практических заданий.

## Типы данных

### Примитивные типы
| Кючевое слово | Описание | Пример |
| --------------------- | -------- | ------ |
| int                   | Целочисленное значение | int foo = 5; |
| float                 | Дробное значение | float иык = 5.3; |
| double                | Дробное значение с повышенной точностью| double pi = 3.2; |
| char                  | Символьное предстваление | char baz = 'a';
| boolean                  | Логическое значение | boolean boo = true;

Обратите внимание на то, что в дробных значения используется точка, а не запятая. В символьном типе используется именно одинарные кавычки, а не двойные.

### Классы
| Кючевое слово | Описание | Пример |
| --------------------- | -------- | ------ |
| String                   | Обычная строка | String foo = "lol"; |

О методах строки можете прочитать [тут](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html)

### Этап 1
[Ловите справку на все этапы](https://www.freecodecamp.org/news/java-getters-and-setters/).
Создайте класс `DataTypes`, объявите в нём приватные свойста для каждой из указанных величин:

1. Счёт в банке
1. Температура на улице
1. Число пи
1. Буква в названии класса в школе
1. Статус рабты чайника

### Этап 2
Для каждого из свойств реализуйте `getter` и `setter`.

### P.S.
Вызывать ничего не нужно, только если захотите протестить

## Ветвления
Давайте попробуем объяснить сыну маминой подруги, что нужно купить в магазине. Техническое задание у него следующее: если будет хлеб, то нужно его купить, иначе он должен взять 2 банки пива (предполагаем, что в магазине всегда есть пиво). Также если будут яйца, то надо купить 10. Ещё надо купить бутылку молока.

### Этап 1
Создать класс `MomsFriendsSon`, в котором объявить 2 метода со следующими сигнатурами:

```java
public void doShopping() {

}

private boolean getAnswerFromConsole(String request) {

}
```

### Этап 2
Узнаём, [как получать данные из консоли](https://www.w3schools.com/java/java_user_input.asp). Далее пишем реализацию для методa `getAnswerFromConsole`. Вы должны запросить что-то типа "В магазе есть хлеб ?". Ожидаемые ответы "y", то есть да, и "n", то есть нет.
После получения ответа проверем его с помощью условия:

```java
System.out.println(request);
String answer = // смотрим по ссылке

if (answer.equals("y")) {
    return true;
} else if (answer.equals("n")) {
    return false;
} else {
    System.out.println("Answer should be 'y' or 'n'");
    System.exit(1);
}
```

В случае неизвестного ответа мы сообщаем об ошибке и выходим из программы.

### Этап 3
В тело метода добавляем следующий код, предварительно прочитав и разобрав его:

```java
boolean bread = this.getAnswerFromConsole("В магазине есть хлеб ?");
boolean eggs = this.getAnswerFromConsole("В магазине есть яйца ?")
boolean milk = this.getAnswerFromConsole("В магазине есть молоко ?")

if (bread) {
    System.out.println("Getting bread");
} else {
    System.out.println("Getting 2 beers");
}

if (eggs) {
    System.out.println("Getting 10 eggs");
}

if (milk) {
    System.out.println("Getting milk");
}
```

### Этап 4
Создаём экземпляр класса `MomsFriendsSon` в методе `main` и вызываем метод `doShopping`:

```java
MomsFriendsSon momsFriendsSon = new MomsFriendsSon();
momsFriendsSon.doShopping();
```

Если у я не ошибся и вы всё првильно сделали, то программа должна предложить вам ответить на три вопроса, после чего вывести правильные ответы.

## Циклы
Пока не сделал, надо пиво допить)