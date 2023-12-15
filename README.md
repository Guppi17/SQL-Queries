# SQL-Queries 
  
<div align="center">
<img src="https://github.com/Guppi17/Guppi17/blob/main/df8e36f90e6a20167f071ed1b6c10e50.gif" width='150'/><img src="https://github.com/Guppi17/Guppi17/blob/main/df8e36f90e6a20167f071ed1b6c10e50.gif" width='150'/><img src="https://github.com/Guppi17/Guppi17/blob/main/df8e36f90e6a20167f071ed1b6c10e50.gif" width='150'/><img src="https://github.com/Guppi17/Guppi17/blob/main/df8e36f90e6a20167f071ed1b6c10e50.gif" width='150'/>
</div>


### Homework-1
Предусловия: установите MySQL Server и MySQL Workbench

1. Скачайте [дампы](https://drive.google.com/drive/u/3/folders/1MC0AttnmlAmugifFlX3hG6pssYZDqpPB) базы данных Hogwarts  
2. Осуществите импорт таблиц, используя Workbench
3. Выполните [задание](https://drive.google.com/drive/u/3/folders/1Lt7CY69nR5awNs_9q0XJOHRti4vJj3Qa) 1 и 2

<br/>
*.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.*    

<br/>


### Homework-2  
Предусловия: создайте аккаунт/окружение в MongoDB Atlas и скачайте MongoDB Compass

1. Создайте новую базу данных Hogwarts
```
use Hogwarts;
```
2. Внутри нее создайте коллекции Characters и Library
```
db.createCollection(""Characters"") 
db.createCollection(""Library"")
```
3. Внутри коллекций создайте документы, которые будут повторять информацию из первого задания 
```
db.Characters.insertMany([
{
char_id: 1,
fname: ""Harry"",
lname: ""Potter"",
age: 11,
faculty: ""Gryffindor"",
patronus: ""Stag"",
book_id: 10
},
{
char_id: 2,
fname: ""Hermione"",
lname: ""Granger"",
age: 11,
faculty: ""Gryffindor"",
patronus: ""Otter"",
book_id: 9
}
])
```
4. Выведите всех персонажей, чей возраст больше 10, но меньше 20 
```
db.Characters.find ({age: {$gt : 10, $lt: 20}})
```
5. Выведите всех персонажей, чей возраст меньше 30 и не равен 11
```
db.Characters.find ({age: {$lt: 30, $ne: 11}})
```
6. Добавьте всем персонажам 1 год к возрасту
```
db.Characters.updateMany({}, { $inc: { age: 1 }})
```
7. Посчитайте общее количество персонажей, чей возраст больше 11
```
db.Characters.count ({age: {$gt: 11}})
```
8. Удалите информацию о книге 'Quidditch Through The Ages'
```
db.Library.deleteOne( { book_name: "Quidditch Through The Ages"} )
```
9. Выведите информацию обо всех в книгах, в названиях которых содержится слово The в любом месте
```
db.Library.find ({book_name: /The/})
```

<br/>
*.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.* ☽ *.·:·.✧ ✦ ✧.·:·.*   
  

<br/>  


## Result  


- [Homework-1](https://docs.google.com/spreadsheets/d/1YimW7aGLZih1QXWi37aAJxj8eEezGWsPFNpASx9LhUU/edit#gid=0)  
  

<div align="center">
<img src="https://github.com/Guppi17/Guppi17/blob/main/yes-hi.gif" width='600'/>
</div>

<br/>
