# Підключення Landing Page як окремий шаблон до існуючої сторінки сайту на WordPress

#### Для початку беремо наш Лендінг(найпростішу зверстану сторінку). У мене він виглядає таким чином:

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20170710.png)

#### 1) Відкриваємо нашу папку LendingPage, та бачимо, що сам лендинг в даному випадку складається з одного index.html файлу та одної assets папки, в якої лежать папки з файлами css та img.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20160427.png)

#### 2) Щоб не завантажувати шаблон сайту зайвими файлами, треба нашу папку з файлами Lending.page перенести до папки /wp-content/.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-26%20135343.png)

#### 3) Перейменуйте файл index.html на index.php

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20161321.png)

#### 4) Тепер відкрийте папку з вашою вже створеною темою на Wordpress, та створіть файл CustomPage01.php, який буде шаблоном для сторінки. Назва може бути довільна, головне, щоб не перетиналося з вже існуючим файлом шаблону.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20153550.png)

#### 5) Відкрийте файл CustomPage01.php відразу на початку вставляємо такий код:

```
<?php /*
Template Name: CustomPage01 */ 
?>
```
![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20155111.png)

#### Такий запис дозволить вивести назву шаблону в адмінці. Назву можете міняти на довільне. Це для зручності орієнтації за шаблонами сторінок.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20155859.png)

#### 6) Далі в цей файл CustomPage01.php вам потрібно скопіювати все, що є у файлі index.php вашого лендинга. Саме в ньому лежатиме лицьова частина вашого лендингу, яка вже потім може посилатися на інші файли (якщо їх у вас багато).
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Responsive Landing Page Template With Flexbox</title>

	<link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet">
	<link href="https://fonts.googleapis.com/css?family=Quicksand" rel="stylesheet">
    <link rel="stylesheet" href="http://maxcdn.bootstrapcdn.com/font-awesome/4.6.0/css/font-awesome.min.css">
    <link rel="stylesheet" href="assets/css/styles.css">

</head>

<body>

	<header>
		<h2><a href="#">Website Logo</a></h2>
		<nav>
			<li><a href="#">Home</a></li>
			<li><a href="#">Products</a></li>
			<li><a href="#">About</a></li>
			<li><a href="#">Contacts</a></li>
		</nav>
	</header>


	<section class="hero">
		<div class="background-image" style="background-image: url(assets/img/hero.jpg);"></div>
		<h1>Responsive Flexbox Template</h1>
		<h3>A freebie by Tutorialzine.</h3>
		<a href="http://tutorialzine.com/2016/06/freebie-landing-page-template-with-flexbox/" class="btn">Download it Here</a>
	</section>


	<section class="our-work">
		<h3 class="title">Some of our work</h3>
		<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices. Morbi vitae pulvinar velit. Sed aliquam dictum sapien, id sagittis augue malesuada eu.</p>
		<hr>

		<ul class="grid">
			<li class="small" style="background-image: url(assets/img/coast.jpg);"></li>
			<li class="large" style="background-image: url(assets/img/island.jpg);"></li>
			<li class="large" style="background-image: url(assets/img/balloon.jpg);"></li>
			<li class="small" style="background-image: url(assets/img/mountain.jpg);"></li>
		</div>
	</section>
	

	<section class="features">
		<h3 class="title">Features and services</h3>
		<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices. Morbi vitae pulvinar velit. Sed aliquam dictum sapien, id sagittis augue malesuada eu.</p>
		<hr>

		<ul class="grid">
			<li>
				<i class="fa fa-camera-retro"></i>
				<h4>Photography</h4>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices vitae pulvinar velit.</p>
			</li>
			<li>
				<i class="fa fa-cubes"></i>
				<h4>Web Development</h4>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices vitae pulvinar velit.</p>
			</li>
			<li>
				<i class="fa fa-newspaper-o"></i>
				<h4>Content Editing</h4>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices vitae pulvinar velit.</p>
			</li>
		</div>
	</section>


	<section class="reviews">
		<h3 class="title">What others say:</h3>

		<p class="quote">Mauris sit amet mauris a arcu eleifend ultricies eget ut dolor. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.</p>
		<p class="author">— Patrick Farrell</p>

		<p class="quote">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices. Morbi vitae pulvinar velit. Sed aliquam dictum sapien, id sagittis augue malesuada eu.</p>
		<p class="author">— George Smith</p>

		<p class="quote">Donec commodo dolor augue, vitae faucibus tortor tincidunt in. Aliquam vitae leo quis mi pulvinar ornare. Integer eu iaculis metus.</p>
		<p class="author">— Kevin Blake</p>

		
	</section>


	<section class="contact">
		<h3 class="title">Join our newsletter</h3>	
		<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam id felis et ipsum bibendum ultrices. Morbi vitae pulvinar velit. Sed aliquam dictum sapien, id sagittis augue malesuada eu.</p>
		<hr>

		<form>
			<input type="email" placeholder="Email">
			<a href="#" class="btn">Subscribe now</a>
		</form>
	</section>

	<footer>
		<ul>
			<li><a href="#"><i class="fa fa-twitter-square"></i></a></li>
			<li><a href="#"><i class="fa fa-facebook-square"></i></a></li>
			<li><a href="#"><i class="fa fa-snapchat-square"></i></a></li>
			<li><a href="#"><i class="fa fa-pinterest-square"></i></a></li>
			<li><a href="#"><i class="fa fa-github-square""></i></a></li>
		</ul>
		<p>Made by <a href="http://tutorialzine.com/" target="_blank">tutorialzine</a>. images courtesy to <a href="http://unsplash.com/" target="_blank">unsplash</a>.</p>
		<p>No attribution required. you can remove this footer.</p>
	</footer>

</body>

</html>

```

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20160228.png)

#### 7) На даний момент вже в адмінці в вашії темі ви побачите новий шаблон. 

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20160502.png)

#### Однак він не виглядатиме, так як заплановано. Причина в тому, що в index.php лендинг будуть прописані відносні шляхи до картинок та стилыв. Тобто, ось так приблизно:

#### Для стилів:
```
<link rel="stylesheet" href="assets/css/styles.css">
```
![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20161355.png)

#### Для картинок:
```
<li class="small" style="background-image: url(assets/img/coast.jpg);"></li>
<li class="large" style="background-image: url(assets/img/island.jpg);"></li>
<li class="large" style="background-image: url(assets/img/balloon.jpg);"></li>
<li class="small" style="background-image: url(assets/img/mountain.jpg);"></li>
```
![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20161640.png)

#### 8) У нас же зараз колишній файл index.php лендінг перетворився на CustomPage01.php і лежить в іншому місці. Відкрийте файл CustomPage01.php та по всьому файлу CustomPage01.php потрібно прописати правильний шлях до папки з лендингом. Робимо це і за підсумком вийде щось подібне:

#### Для стилів:
```
<link rel="stylesheet" href="<?php bloginfo('template_directory') ?>/styles01.css">
```

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-28%20162649.png)

#### Для картинок:

```
<li class="small" style="background-image: url(/img/coast.jpg);"></li>
<li class="large" style="background-image: url(/img/island.jpg);"></li>
<li class="large" style="background-image: url(/img/balloon.jpg);"></li>
<li class="small" style="background-image: url(/img/mountain.jpg);"></li>
```
![](https://github.com/ssonyau/)

#### Якщо проставили шлях до папки з лендингом скрізь файлом CustomPage01.php правильно, то тепер в адмінці можете сміливо вибирати шаблон сторінки і все буде працювати як треба.

![](https://github.com/ssonyau/Landing-Page-simple-Wordpress/blob/main/Screenshot%202023-04-27%20111242.png)

