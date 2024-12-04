﻿# My Learning
Все обучающие курсы которые имеются в наличии:
1. Git;
2. Pandas;
3. Parsing;
4. Python;
5. Visualisation;
&&& others &&&
&&

### Документация для анализа работы и визуализации показателей салонов красоты
Краткая суть проекта

### Описание
Подробное описание проекта

#### Договорённости:
1. Названия ПАПОК с проектами пишутся в НИЖНЕМ регистре латинскими буквами со знаком нижнего подчёркивания "_" между словами.
	(например, "beauty_salon")
2. Названия КОММИТОВ пишутся в НИЖНЕМ регистре латинскими буквами, каждое слово с БОЛЬШОЙ буквы со знаком нижнего подчёркивания "_" между словами.
	(например, "Added_Changed_In_Beauty_Salon.jpnb")

### Jupyter Notebooks, csv and xlxs files, jpg and png visual
Типы файлов в проекте

### Разные пути к разным репозиториям на диске (ненужное для проекта - удалить)
cd ~
cd /c/Users/Андрей/my_learning
cd my_learning/spektr
cd c/Users/Андрей/my_learning/spektr

### Пример запроса команды для терминала о версии библиотеки
print pandas.__version__ (pip show pandas)
print json.__version__

### Памятка по созданию нового проекта

#### 1. Типовая структура проекта.
Папку "FOLDER_TEMPLATE" с типовой структурой проекта копируем и переименовываем в новом проекте по его названию из репозитория по адресу: c/Users/Андрей/my_learning/spektr

#### 2. Файл .GITIGNORE
Шаблон файла .GITIGNORE находится по этому же адресу - просто копируем его в новый проект

#### 3. Виртуальное окружение - последовательность команд в терминале:

##### 3.1. Создаётся для каждого создаваемого проекта
3.1.1. Заходим в папку с проектами: "cd c/Users/Андрей/my_learning" или просто "cd my_learning"
3.1.2. Внутри этой папки создаём папку для нового проекта: "mkdir spektr"
3.1.3. Переходим в созданную папку: "cd spektr"
3.1.4. "virtualenv venv"
3.1.5. Активируем виртуальное окружение: "source venv/bin/activate" --> в начале строки появилась надпись , что означает, что в этом проекте установлено виртуальное окружение.
	3.1.5.1. Как вариант - ("source venv/Scripts/activate")
3.1.6. По окончании работы с проектом (в случае перехода в другой проект для работы): "deactivate".

##### 3.2. Во время работы в КАЖДОМ проекте устанавливаем необходимые модули библиотек для настройки виртуального окружения
3.2.1. Например, "pip install pandas"
3.2.2. Чтобы узнать версию конкретной библиотеки в этом виртуальном окружении: "pandas --version"

##### 3.3. Файл REQUIREMENTS.TXT
3.3.1. Этот файл содержит список всех библиотек, используемых в проекте
3.3.2. Чтобы узнать какие библиотеки используются в текущем проекте: Terminal --> "pip freeze"
3.3.3. Чтобы создать список библиотек проекта: Terminal --> "pip freeze > requirements.txt"
3.3.4. Чтобы установить одной командой все библиотеки необходимые для работы проекта на другую машину: Terminal --> "pip install -r requirements.txt"

#### 4. Репозиторий

##### 4.1. Локальный репозиторий
4.1.1. Под каждый проект создаём новый репозиторий
4.1.2. Заходим в папку с проектом: "cd ~ --> cd c/Users/Андрей/my_learning/spektr" или просто "cd ~ --> cd my_learning/spektr"
4.1.3. "git init"
4.1.4. (Чтобы увидеть скрытые файлы для Мас --> "Command + Shift + '.'")
4.1.5. Основные команды при работе с локальным репозиторием:
	git status - проверка статуса файлов;
	git add . (git add *) - сохранить изменения одного или нескольких или всех файлов;
	git commit -m 'Write_Commit_For_Last_Changing' - создание Коммита (название изменения);
	git restore file_name.py (restore test.py) - восстановление нежелательных изменений (откат к последнему созданному коммиту);
	git checkout commit_name - восстановление ранее сделанных изменений (откат к более ранним коммитам);
		git log --> copy commit_hash () --> "q" --> checkout (paste commit_hash) --> ENTER;
	git push - передача изменений на удалённый репозиторий (GITHUB);
	git pull - получение проекта из удалённого репозитория на локальный.

##### 4.2. Удалённый репозиторий (GITHUB)
4.2.1. Создание нового репозитория:
	Заходим в аккаунт GitHub --> Заходим в список репозиториев --> В правом верхнем углу: "Создать новый репозиторий - NEW" --> Заполняем необходимые поля (Название(Name), Описание(Description), тип репозитория (приватный или открытый), галочки для создания README.md и .GITIGNORE ВЫКЛЮЧАЕМ) --> СОЗДАТЬ РЕПОЗИТОРИЙ (CREATE REPOSITORY)
4.2.2. Последовательно копируем и вставляем в терминал команды:
	"git remote add origin https://github.com/ayaweb7/spektr" --> "git branch -M origin" --> "git push -u origin main"
	
##### 4.3. Аутентификация
Если SSH-ключ отсутствует, то проходим по всему списку:
4.3.1. GitHub --> Profile --> Settings --> SSH and GPG keys --> "Generating a new SSH key" --> Copy "ssh-keygen -t ed25519 -C ayaweb7@gmail.com"
4.3.2. Terminal --> Paste --> Enter Password Two Times --> "eval "$(ssh-agent -s)"" --> "ssh-add c:/Users/Андрей/my_learning .ssh/id_ed25519"
4.3.3. Создать файл конфигурации .CONFIG: --> "touch ~/.ssh/config" (или открыть существующий "open ~/.ssh/config") --> внести изменения и сохранить
4.3.4. Генерируем новый SSH-ключ: "clip < ~/.ssh/id_ed25519.pub"
4.3.5. GitHub --> Profile --> Settings --> SSH and GPG keys --> New SSH Key --> Comment --> Paste --> ENTER --> ADD SSH KEY
4.3.6. Testing your SSH connection: Terminal --> "ssh -T git@github.com"

Если SSH-ключ уже существует, то пропускаем пункты, по созданию ключа: ... копируем, изменяем, сохраняем, проверяем.

### : Terminal - Горячие клавиши:
	cd ~ - Переход в домашнюю папку из любой текущей папки любого проекта
		(option+N for Mac; alt+N for Win);
	cd .. - Переход на один уровень вверх;
	Command + Shift + "." - Показать/Скрыть скрытые файлы (на Мас);
	Ctrl + D/Z - Выход из консоли Python на Мас/Windows;
	Command + K - очистка окрана терминала;
	cd (beginning folder) + Tab - ;
	ls - отображение файлов в папке;
	ls -la - то же с флагами "l" - в виде списка, "a" - вместе со скрытыми файлами;
	open folder - Открыть папку в Finder;
	code file.py - Открыть файл в VSCode;
	Стрелки "верх, вниз" - Поиск ранее введённых команд;
	"source venv/bin/activate" - активация виртуального окружения;
	"deactivate" - дезактивация виртуального окружения

### Jupyter Notebook - Горячие клавиши:
	"Ctrl+Enter"/"Shift+Enter" - Выполнение ячейки (Mac/Windows);
	"Ctrl+/"- Комментирование / раскомментирование строки;
	"Ctrl+A" - Создать ячейку ВЫШЕ;
	"Ctrl+B" - Создать ячейку НИЖЕ;
	"Ctrl+M" - Объединить выделенные ячейки;
	"Ctrl+C" - Скопировать выделенную ячейку;
	"Ctrl+V" - Вставить содержимое ячейки (или ячейку);
	"Ctrl+X" - Вырезать;
	"Ctrl+S" - Сохранить изменения;
	" """ """ " - Многостраничный комментарий;
	Стрелки:
		"Вверх" - на начало первой строки в ячейке;
		"Вниз" - на конец последней строки в ячейке;
		"Влево" - на начало текущей строки в ячейке;
		"Вправо" - на конец текущей строки в ячейке;
	- ;
	

