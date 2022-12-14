# **Инструкция по использованию системы контроля версий Git**

![Крошка Ши](KroshkaShi.jpeg)

## Что такое Git

Программа Git - система контроля версий.

## Инициализация репозитория

Чтобы инициализировать (создать) новый репозиторий нужно ввести в терминале команду:

    git init

## Проверка состояния репозитория

Чтобы проверить сотсояние репозитория нужно ввести команду:

        get status
        
 ## Добавление изменений в индекс

 Чтобы добавить изменения в индекс для следующего коммита нужно ввести команду:
     
    git add <filename> 

## Фиксация изменений

Чтобы зафиксировать изменения и увидеть информацию о появлении новой версии нужно ввести команду:
    
    git commit

## Фиксация изменений с комментарием

Чтобы оставить комментарий, описание изменения необходимо ввести команду:
    
    git commit -m "message"

## Добавление и фиксация изменений

Чтобы не вводить последовательно две команды на внесение изменений и их фиксацию можно воспользоваться командой:

    git commit -am "message"

NB! Данная команда добавит все имеющиеся изменения. Лучше не использовать для большого количества коммитов и следовать принципу атомарности коммитов, т.к. иначе потом будет сложно отслеживать и вносить изменения при необходимости.

## Просмотр журнала изменений

Чтобы вывести список всех коммитов в хронологическом порядке необходимо ввести команду:

    git log

## Просмотр краткого журнала изменений

Можно также вывести список всех коммитов в хронологическом порядке, но только с самой важной информацией(hash+message):

    git log --oneline

## Просмотр журнала изменений при нахождении не в последнем актуальном коммите

При перемещении между коммитами и нахождении не в последнем актуальном коммите, при вызове журнала отобразятся только коммиты, актуальные для него. Чтобы вывести весь краткий журнал изменений необходимо ввести команду:

    git log --online --all

При этом будет отмечено актуальное местоположение (HEAD) и последняя актуальная версия (master). NB! Важно вернуть потом к положению master.

## Перемещение между коммитами

Для перемещения между коммитами используется команда:

    git checkout <hash>

## Вычисление разницы между состояниями файла

Для вычисления разницы между текущей версией и уже зафиксированной необходимо ввести команду:

    git diff

Также можно посмотреть разницу между двумя конкретными коммитами введя последовательно:

    git diff <hash>
    
    git diff <hash2>

# Домашнее задание 2

## Ветвление

Ветки в гит нужны для одновременной работы над разными частями проекта или для тпроработки каких-то отдельных частей проекта, на мешая при этом его работе.

## Создание новой ветки

Чтобы создать новую ветку нужно ввести команду:

    git branch <branchname>

После создания новой ветки можно проверить список веток с помощью команды:

    git branch

Ветка, на которой вы находитесь в данный момент, будет отмечена звездочкой. 

## Переход между ветками

Чтобы перейти на другую ветку необходимо ввести команду:

    git checkout <branchname>

После перехода лучше проверить, что он осуществлен, вызвав список веток командой git branch.

## Слияние

Чтобы слить две ветки необходимо ввести команду:

    git merge <branchname>

    NB! Команда вводится на той ветке, куда вы хотите добавить изменения с другой ветки. Т.е. если у вас две ветки, 1 и 2, и вы хотете слить ветку 2 с веткой 1, то команда слияния будет вводиться на ветке 1 и выглядеть будет так: git merge 2.

### Конфликты слияния

Если при слиянии двух версий одна и та же строчка написана по-разному, то возникнет конфликт слияния. При этом git добавит оба варианта и предложит четыре варианта развития событий, из которых необходимо будет выбрать:

* оставить версию главной ветки
* оставить версию той ветки, которую сливаем
* сравнить обе версии
* оставить обе версии

После слияния необходимо сохранить изменения и закоммитить их.В случае, если конфликта не было, коммит создастся автоматически.

# Окончание домашнего задания



## Удаленные репозитории

Удаленные репозитории - это ....очень полезная штука









