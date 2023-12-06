# Это шпаргалка по работе с Git и Git-Hub


## Навигация в командной строке: 
* pwd - показать текущую директорию
* ~ - домашняя директория
* .. - родительская директория
* . - текущая директория
* ls - отобразить содержимое директории (флаг -a покажет объекты с запрещёнными символами в названии)
* cd - сменить директорию, после команды указать путь до нужной директории

## Управление файлами в командной строке
* touch - создание файла (touch <название файла> <местоположение файла>)
* cp - копирование файла (синтаксис аналогичный touch)
* mkdir - создание директории (флаг -p - создать структуру директорий)
* mv - переместить файл или директорию
* cat - чтение файлов (только .txt)
* rm - удаление файла 
* rmdir - удаление дирректории (удаляет пустую директорию, для последовательного удаления всех элементов директории с последующим удалением самой директории: rm -r)


## Эффективная работа с коммандной строкой
* && - разделитель между командами для множественного вызова (пример: cd~ && ls -a - переход к домашней директории и отображение её содержимого)
* Клавиши стрелок ↑↓ - обращение к ранее использованным командам
* Клавиша Tab - автоматическое заполнение команды, двойной Tab - вывод списка доступных команд

## Работа с Git: создание репозиториев, коммит 
* git init - сделать текущую папку репозиторием
* rm -rf .git - разгитить папку (удалить скрытую папку .git)
* git status - проверить состояние репозитория
* git add - подготовить файл к сохранению (используют флаги --all или . для сохранения сразу всех объектов в текущей директории)
* git commit - сделать коммит = сохранить изменения (с помощью флага -m"<комментарий к изменению>" можно добавить комментарий)
* git log - просмотр истории коммитов (--oneline - получить сокращённый лог)
 
## Синхронизаия локального и удалённого репозиториев в Git-Hub
* ssh-keygen - генерация SSH пары (ssh-keygen -t ed25519 -C"имя почты к которой привязан аккаунт" **ИЛИ** ssh-keygen -t rsa -b 4096 -C"имя почты к которой привязан аккаунт")
* pbcopy - копирование потока данных в буффер обмена (pbcopy < <путь до файла>), эти данные нужно вставить на сайте [Git-Hub](https://github.com "Сайт Git-Hub") в разделе Settings->SSH and GPG keys->New SSH key в поле **key**
* ssh -T git@github.com - проверить подлинность ключа
* git remote add - привязать удалённый репозиторий к локальному (передаём в команде два параметра - имя удалённого репозитория origin, и его URL)
* git remote -v - убедиться, что репозитории связаны
* git push - отправить изменения на удалённый репозиторий

## Хэши, лог, статусы файлов
* __Хеш__ — основной идентификатор коммита 
    * Свойства хеша: если дважды получить хеш для одного набора данных, результат будет одинаковым.
    * Если изменить хоть что-то в исходных данных, хеш изменится.
   