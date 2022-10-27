# Project-2 (HW-03)
1. Основываясь на том, что доступ к коду создаваемого нашей командой приложения должен быть ограничен, выберите подходящий хостинг для репозиториев с кодом среди работающих с Git.

# Answer:

github.com

2. Продумайте, каков будет порядок внесения изменений в основную кодовую базу (какой будет флоу), какое именование веток будет использоваться.

# Answer: 
Изменения вносятся в основную ветку master на основе результатов недельного спринта. Кроме ветки master используются еще дополнительно ветки, которые поименованы согласно с именами девелоперов из рабочих групп Senior, Middle и Junior. Рабочая группа Senior состоит из одного сотрудника Bob, рабочая группа Middle состоит из одного сотрудника Alice, рабочая группа Junior состоит из одного сотрудника John. Участники рабочих групп Senior и Middle зарегистрированы в проекте как коллабораторы и имеют прямой доступ к своим веткам и ветке master. Участники рабочей группы Junior не зарегистрированы в проекте как коллабораторы, требуется создать pull request и провести ревью кода другими сотрудниками, чтобы смерджить их код в ветку master. По результатам недельного спринта изменения применяются сначала участниками группы Senior, во вторую очередь участниками группы Middle, и в последнюю очередь участниками Junior.

3. Настройте себе среду разработки: выберите удобный для вас редактор кода — IDE. Настройте доступ к репозиторию по ключу, а также настройте следующие параметры для работы с Git (git config):
имя и электронная почта пользователя;
алиас history для команды log --graph. То есть при вызове команды git history должна выполняться команда git log --graph (git history — не встроенная команда).

# Answer:
[petr@junibox projects]$ more  ~/.gitconfig

[gpg]
        program = gpg

[user]
        email = petr.akimov@yahoo.com
        
        name = Petr Akimov

[commit]
        gpgsign = true

[alias]
        history = log --graph


4. Создайте на выбранном в п. 1 хостинге репозиторий для команды и добавьте туда первый файл — полученный в п. 3 git config.

# Answer:
https://github.com/petr-akimov/Project-2/blob/master/src/.gitconfig

5. Напишите небольшую документацию для будущих сотрудников (редактор остается на ваше усмотрение). В ней должно быть указано:
где располагается репозиторий с кодом, как посмотреть существующий код;
как устроен процесс внесения своих изменений в основную кодовую базу;
каковы правила именования веток;
как настроить свою среду разработки, требуется прикрепить ссылку на лежащий в проекте конфиг;
инструкция для младших сотрудников по слиянию веток, какие команды надо выполнить, чтобы:

- создать свою ветку;  
- внести изменения в нее;
- слить эти изменения с основной кодовой базой.

# Answer: 
Изменения вносятся в основную ветку master на основе результатов недельного спринта. Кроме ветки master используются еще дополнительно ветки, которые поименованы согласно с именами девелоперов из рабочих групп Senior, Middle и Junior. Рабочая группа Senior состоит из одного сотрудника Bob, рабочая группа Middle состоит из одного сотрудника Alice, рабочая группа Junior состоит из одного сотрудника John. Участники рабочих групп Senior и Middle зарегистрированы в проекте как коллабораторы и имеют прямой доступ к своим веткам и ветке master. Участники рабочей группы Junior не зарегистрированы в проекте как коллабораторы, требуется создать pull request и провести ревью кода другими сотрудниками, чтобы смерджить их код в ветку master. По результатам недельного спринта изменения применяются сначала участниками группы Senior, во вторую очередь участниками группы Middle, и в последнюю очередь участниками Junior.

# Инструкция для младших сотрудников по слиянию веток, какие команды надо выполнить, чтобы:

- создать свою ветку; 
сделать fork публичного репозитория https://github.com/petr-akimov/Project-2/ , зайдя на сайт, нажмите кнопку fork.

Склонировать репозиторий со своей копии на GitHub в локальную и далее работать ТОЛЬКО с локальной копией, в Вашей собственной новой уникальной ветке 
(git checkout -b <имя.фамилия разработчика>)
 
- внести изменения в нее;
После изменений и перед загрузкой файлов в Ваш личный репозиторий на GitHub добавьте новые файлы, сделайте коммит локально 
(git add . , git commit -S -m  "Some comment")

git push -u origin <new_branch>

Откройте свой репозиторий на сайте github.com, убедитесь, что внесенные Вами изменения корректны. Создайте пулл-реквест (compare & pull Request / Create pull request)

- слить эти изменения с основной кодовой базой.

Изменения проходят ревью другими сотрудниками, после чего по результатам ревью происходит слияние с основной кодовой базой

6. Направьте документацию, разработанную в п. 5, ментору на проверку.
