1)На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing

Буду работать в репозитории:
git branch Postman
git branch Jmeter
git branch Checklists
git branch Bag_Reports
git branch SQL
git branch Charles
git brahch Mobile_testing

2) Запушить все ветки на внешний репозиторий:
git push -u origin --all

3) В ветке Bag Reports сделать текстовый документ со структурой баг репорта:
git checkout Bag_Reports
touch bag.txt
vim bag.txt


[YMETRO-17] Некорректные параметры максимального масштаба схемы метро
Описание:
Можно приближать схему до нечитаемого состояния/вида.
Шаги воспроизведения:
Открыть схему метро: https://qa-metro.stand-2.praktikum-services.ru/
Кликнуть на значок «+» более 6 раз или увеличивать скроллом, пока не перестанет увеличиваться.
Фактический результат: Схема увеличилась до нечитаемого состояния/вида.
Ожидаемый результат: Через 3-6 кликов схема перестаёт увеличиваться (зависит от города).
Окружение:
Windows 8, браузер Google Chrome Версия 77.0.3865.90
Приоритет: Средний
I
esc
:wq
enter

git add .
git commit -m "add information to the bag.txt"

4) Запушить структуру багрепорта на внешний репозиторий: git push
5) Вмержить ветку Bag Reports в Main:
git checkout main
git merge Bag_Reports
6) Запушить main на внешний репозиторий: git push -u origin main
7) В ветке CheckLists набросать структуру чек листа:

git checkout CheckLists
touch list.txt
vim list.txt
I

Structure of a checklistStructure of a checklist:
1. Build
2. Environment
3. test date
4. Tester
5. Test Type
6. Checking
7. Result

esc
:wq
enter

8) Запушить структуру на внешний репозиторий:
git add .
git commit -m "the structure of the checklist"
git push

9)На внешнем репозитории сделать Pull Request ветки CheckLists в main:
перешла в гитхабе на main ветку, выбрала вкладку pull request, затем new pull request, выбрала ветку Checklists. 
Осуществила merge

10) Синхронизировать Внешнюю и Локальную ветки Main:
git checkout main
git fetch
git pull

конец
