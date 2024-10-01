## Лабораторная работа 1

Разминка лабораторной работы №1:

1. Создайте новый файл с именем `script.bash`

```bash
touch script.bash
```

*Делаю я, это, очевидно, через терминал - Ctrl+Alt+T.*

2. Откройте созданный файл `script.bash` для редактирования. Стандартный текстовый редактор в Linux Ubuntu это `gedit`. Выполните в терминале

```bash
gedit script.bash
```

*Естественно, это не работает - чтобы сработало, нужно ещё установить редактор Gedit командой ```sudo apt install gedit```. Тогда файл открывается.*

3. Впишите следующий скрипт

```bash
#!/bin/bash

echo "Welcome to ITMO University"
```

4. Сохраните файл. Закройте текстовый редактор `gedit`. Запустите bash-скрипт, выполнив в терминале

```bash
bash script.bash
```

5. Если вы все сделали верно, то в терминале должна отобразиться строка `Welcome to ITMO University`.

*Всё верно, так и есть.*

### Задача

Модифицируйте файл `script.bash` так, чтобы при его запуске в терминале в виде

```bash
bash script.bash Vasya Pupkin
```

Вывод был

`Welcome, Vasya Pupkin`

*Hint:* Скрипт должен работать для любых имен, даже если это Benedict Timothy Carlton Cumberbatch.

### Решение

В файле 'script.bash' нужно написать следующий код:

'''
#i/bin/bash

echo "Welcome, $*, you don't exist"
'''

*'$*' - специальная переменная, которая объединяет переданные аргументы в одну строку, а в конце "you don't exist" я подписал просто чтобы проверить, сможет ли оно распаковать два аргумента сразу. Сможет:*

![image](https://github.com/mxrget/linux-university-lab-1/blob/main/welcome-lab1.png)
