# Занятие №1

Проходим [экскурс](https://losst.ru/42-komandy-linux-kotorye-vy-dolzhny-znat) по линукс. Достаточно впитать первые 9 команд, их вам пока хватит.
Смотрим [это видео](https://www.youtube.com/watch?v=zZBiln_2FhM) до секции про `.gitignore`, и повторяем всё, что делает автор (на сервере, конечно).
После приступаем к инструкциям ниже:

1. Создать аккаунт на `github`, если это ещё не сделано
1. Нажать на кнопку `Fork`, которая находится в правом верхнем углу
1. Добавить `ssh` ключ сервера в аккаунт:
1. На сервере в папке `~/code` склонировать репозиторий
1. Писать код

## Как добавить `ssh` ключ в `github` аккаунт
На сервере пишем:
```bash
ssh-keygen
```

Соглашаемся со всем предложенным и просто спамим `Enter`.
Вводим следующую команду:
```bash
cat ~/.ssh/id_rsa.pub
```

Вы увидите много текста, его весь нужно скопировать.

Далее заходим в настройки вашего аккаунта, в списке слева ишем
`Access` -> `SSH and GPG keys`. Выбираем `New SSH key`, 
в названии пишем `programming-school`, а в поле ключа вставляем то, 
что скопировали на сервере. Подтверждаем.

## Как склонировать репозиторий
Помотреть ваш репозиторий можно по ссылке 
`https:/github.com/<username>/programming-school-2022`, 
где `<username>` ваш логин на `github`.

Для клонирования сайт открывать необзательно, достаточно ввести 
следующие команды на сервере:
```bash
cd ~/code
git clone git@github.com:<username>/programming-school-2022.git
cd programming-school-2022
```

Поздравляю, вы склонировали репозиторий и открыли его на сервере!

## Как писать код
### Разработка
Сначала перейдите в папку `programming-school-2022`:
```bash
cd ~/code/programming-school-2022
```

Теперь вы можете перейти в папку нужного таска, например:
```bash
cd task2
```

Для каждого из заданий нужно создать папку и перейти в неё:
```bash
mkdir problem1 && cd problem1
```

Осталось создать файл `Main.java` и писать код:
```bash
nvim Main.java
```

### Сохранение
Для сохранения кода в `github` необходимо использовть 3 команды:
* `g add` - добавляет указанные файлы в контроль версий
* `g commit` - сохраняет созданные изменеия в файлах, которые были добавлены через `g add`
* `g push` - отправляет все изменения в репозиторий на `github`

Алгоритм работы у вас такой:
Добавить файлы, сохранить изменения, отправить в `github`:

```bash
g add . # Добавит все изменённые файлы в текущей папке
g commit -m 'Adding solution for task2 exersice1' # Сохранит добавленные изменения
g push origin main # Отпарвит ваши изменения в репозиторий на github
```