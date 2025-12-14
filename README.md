# Лабораторная работа №6
## Система контроля версий

Цель лабораторной работы: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удаленным репозиторием.

### Ход работы

#### 1. Настроен клиент Git.
```
git config --global user.name "4416 Ананин В.М."
git config --global user.email "vladananin1234@gmail.com" 
```
![Настройка гит](pictures/image-1.png)

#### 2. Клонирован личный репозиторий на компьютер
```
git clone <https://github.com/Fbsusb/LR6.git>
```
![Клонирование личного репозитория на компьютер](pictures/image-2.png)

#### 3. Добавлен файл через интерфейс GitHub. Подтянуты изменения в локальный репозиторий.
```
git pull
```
![Добавлен файл](pictures/image-3.png)
![Добавлены изменения в локальный репозиторий](pictures/image-4.png)

#### 4. Создана ветка conflict-test
```
git checkout -b conflict-test
```
![Создана ветка conflict-test](pictures/image-5.png)

#### 5. Внесение изменений в файле README.md ветки conflict-test.
```
git add README.md
git commit -m "Изменил строку в README в ветке conflict-test"
```
![Внесение изменений в файле README.md ветки conflict-test.](pictures/image-7.png)

#### 6. Внесение изменений в файле README.md ветки master
```
git checkout master
git add README.md
git commit -m "Изменил ту же строку в README в ветке master"
```
![Внесение изменений в файле README.md ветки master](pictures/image-8.png)

#### 7. Попытка слияния веток.
```
git merge conflict-test
```
![Попытка слияния веток](pictures/image-9.png)
![Конфликт веток](pictures/11.png)

#### 8. Разрешение конфликта 
```
git add README.md
git commit -m "Разрешил конфликт между master и conflict-test"
```
![Разрешение конфликта ](pictures/image-10.png)

#### 9. Удаление ветки 
```
git branch -d conflict-test 
```
![Удаление ветки](pictures/image-11.png)

#### 10. Откаты и отчет
Фиксация изменений в файле mergefile.txt
```
git add .
git commit -m "Добавил полезную функцию 1"
git commit -m "Добавил полезную функцию 2" 
```
![Фиксация изменений в файле mergefile.txt](pictures/image-13.png)

Откат второго коммита 
```
git log --oneline
git revert git revert a4ecfae
```
![Откат второго коммита ](pictures/image-14.png)

#### 11. Получена история операций в форматированном виде.
```
git log --pretty=format:"%h - %ad - %an : %s" --date=short
```
![История операций в форматированном виде.](pictures/image-15.png)

#### 12. Финальная версия отчета.
```
git status
git add .
git commit -m "Добавлена финальная версия отчёта"
```
![Финальная версия отчета.](pictures/image-16.png)

Выводы: изучены базовые возможности системы управления версиями, получен опыт работы с Git Api, получен опыт работы с локальным и удаленным репозиторием.
