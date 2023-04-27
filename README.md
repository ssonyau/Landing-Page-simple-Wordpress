# Підключення Landing Page як окремий шаблон до існуючої сторінки сайту на WordPress

#### Для початку беремо наш Лендінг(найпростішу зверстану сторінку). У мене він виглядає таким чином:

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20170710.png)

#### 1) Відкриваємо нашу папку LendingPage, та бачимо, що сам лендинг в даному випадку складається з одного index.html файлу та одної assets папки, в якої лежать папки з файлами css та img.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20160427.png)

#### 2) Щоб не завантажувати шаблон сайту зайвими файлами, треба нашу папку з файлами Lending.page перенести до папки /wp-content/.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-26%20135343.png)

#### 3) Перейменуйте файл index.html на index.php

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20161321.png)

#### 4) Тепер відкрийте папку з вашою вже створеною темою на Wordpress, та створіть файл page-1.php, який буде шаблоном для сторінки. Назва може бути довільна, головне, щоб не перетиналося з вже існуючим файлом шаблону.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20161753.png)

#### 5) У page-1.php відразу на початку вставляємо такий код:

```
<!--?php
/*
Template Name: Ще одна сторінка
*/
?-->
```
![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20162457.png)

#### Такий запис дозволить вивести назву шаблону в адмінці. Назву можете міняти на довільне. Це для зручності орієнтації за шаблонами сторінок.

#### 6) Далі в цей файл page-1.php вам потрібно скопіювати все, що є у файлі index.php вашого лендинга. Саме в ньому лежатиме лицьова частина вашого лендингу, яка вже потім може посилатися на інші файли (якщо їх у вас багато).

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20162808.png)

#### 7) На даний момент вже в адмінціб в вашії темі ви побачите новий шаблон. 

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20163312.png)

#### Однак він не виглядатиме, так як заплановано. Причина в тому, що в index.php лендинг будуть прописані відносні шляхи до картинок, скриптів та іншого. Тобто. ось так приблизно:
```
<link rel="stylesheet" href="assets/css/styles.css">
```
![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-26%20144944.png)

#### 8) У нас же зараз колишній файл index.php лендінг перетворився на page-1.php і лежить в іншому місці. Відкрийте файл page-1.php та по всьому файлу page-1.php потрібно прописати правильний шлях до папки з лендингом (у прикладі це папка LandingPage, яка лежить у папці /wp-content/). Робимо це і за підсумком вийде щось подібне:
```
<link rel="stylesheet" href="/wp-content/LendingPage/assets/css/styles.css">
```

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-26%20145600.png)

#### Якщо проставили шлях до папки з лендингом скрізь файлом page-1.php правильно, то тепер в адмінці можете сміливо вибирати шаблон сторінки і все буде працювати як треба.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20111242.png)

