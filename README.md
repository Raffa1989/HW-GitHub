Окружение MAC OC

Предварительно создать внешний репозиторий. Для работы клонировать его через терминал на локалку.

1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing
```bash
git branch Postman
git branch Jmeter
git branch CheckList
git branch Bug_Reports #  именно так
git branch SQL
git branch Charles
git branch Mobile_testing
```
2. Запушить все ветки на внешний репозиторий
```bash
git push -u --all
```
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта
```bash
git checkout Bug_Reports
vim pattern_bug_report.txt
#  прописываю 
1. Summary
2. Project
3. Component
4. Version
5. Severity
6. Priority
7. Steps to Reproduce
8. Actual Result
9. Expected Result
10. Additional Information
#  ESC 
#  :wq
```
4. Запушить структуру багрепорта на внешний репозиторий
```bash
git add .
git commit -m "bug report"
git push
```
5. Вмержить ветку Bag Reports в Main
```bash
git merge Bug_Reports
```
6. Запушить main на внешний репозиторий.
```bash
cd ..
git add .
git commit -m "merge vetok"
git push
```
7. В ветке CheckLists набросать структуру чек листа.
```bash
git checkout CheckList
vim pattern_checklist.txt
#  прописываю
1. ID
2. Tester Action
3. Actual Result
4. Comment
#  ESC 
#  :wq
```
8. Запушить структуру на внешний репозиторий
```bash
git add .
git commit -m "checlistt"
git push
```
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
```bash
Интуитивно понятно (в нужном  внешнем репозитории сверху будет кнопка для pull. 
Далее кликаем по зеленым кнопкам и все сохраняем)
```
10. Синхронизировать Внешнюю и Локальную ветки Main
```bash
git checkout master
git pull
```
