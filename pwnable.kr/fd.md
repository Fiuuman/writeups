# [pwnable.kr](https://pwnable.kr) | [fd](https://pwnable.kr/play.php)

# Description
![desc](./imgs/fd-desc.webp)

# Connect
```
ssh fd@pwnable.kr -p2222
```
![desc](./imgs/fd-connect.webp)
```
password: guest
```
# Answer
Посмотрим на код: 
![desc](fd-code.webp)
Мы видим что у нас есть функция main, которая в свою очередь принимает агрументы(некий пароль). Что нам нужно сделать? В глаза сразу бросается переменная:
```
int fd = atoi( argv[1] ) - 0x1234
```
Что она значит? Функция atoi берет первый передаваемый аргумент в программу и вычитает из него 0x1234. Что такое 0x1234? Если посчитать это на Python, то у нас будет целое число, давайте попробуем: 
```
```