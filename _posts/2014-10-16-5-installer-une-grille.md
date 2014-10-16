---
layout: post
title:  "Installer une grille"
date:   2014-10-16 09:45:00
categories: html
tags: html grille css
---


## utiliser du code préexistant

Le web s’est beaucoup fait par mimétisme et par progression collective. Le fait d’utiliser des morceaux de code trouvés de part et d’autre du web est une pratique courante, surtout quand on est débutant. 

**Cela évite souvent de réinventer la roue.**

## la grille

Il existe de nombreux systèmes de **grille** pour `HTML/CSS` et même parfois pour certaine avec du `JavaScript`

![Responsive Grid System](/3dvg-web/images/responsivegridsystem.png)

Nous utiliserons le système `Responsive Grid System`, dont le code source et la documentation sont disponible à cette adresse [responsivegridsystem.com][responsivegridsystem] sous license *Creative Commons Attribution 3.0*.

## mise en place

l’enjeu de cette exemple n’est pas *l’explication* du fonctionnement de la grille, mais sur *la mise en place d’un code pré-existant* trouvé sur internet. La grille n’est donc qu’un cas particulier. On expliquera plus tard (quand on aura de plus solide bases en CSS) les principes fondamentaux d'une grille CSS

## copier/coller !

On suit les instructions de l’exemple en copiant d’une part le code HTML. on remarque que le code HTML ne contient ni balises `head` `body` ou même `html`. Quand ce n’est pas précisé dans la documentation, cela signifie que l’on doit le coller dans le `body`.

{% highlight HTML %}

<div class="section group">
	<div class="col span_1_of_3">
	This is column 1
	</div>
	<div class="col span_1_of_3">
	This is column 2
	</div>
	<div class="col span_1_of_3">
	This is column 3
	</div>
</div>

{% endhighlight %}

et ensuite, on copie colle le CSS, dans un fichier que l’on aura préparé et associé. Il faut donc créer au préalable un fichier CSS,
et l’associer. (voir l’article sur **l’entête du document HTML**)

{% highlight CSS %}

/*  SECTIONS  */
.section {
	clear: both;
	padding: 0px;
	margin: 0px;
}

/*  COLUMN SETUP  */
.col {
	display: block;
	float:left;
	margin: 1% 0 1% 1.6%;
}
.col:first-child { margin-left: 0; }


/*  GROUPING  */
.group:before,
.group:after {
	content:"";
	display:table;
}
.group:after {
	clear:both;
}
.group {
    zoom:1; /* For IE 6/7 */
}

/*  GRID OF THREE  */
.span_3_of_3 {
	width: 100%;
}
.span_2_of_3 {
	width: 66.1%;
}
.span_1_of_3 {
	width: 32.2%;
}

/*  GO FULL WIDTH AT LESS THAN 480 PIXELS */

@media only screen and (max-width: 480px) {
	.col { 
		margin: 1% 0 1% 0%;
	}
}

@media only screen and (max-width: 480px) {
	.span_3_of_3 {
		width: 100%; 
	}
	.span_2_of_3 {
		width: 100%; 
	}
	.span_1_of_3 {
		width: 100%;
	}
}

{% endhighlight %}

Il est donc aisé de copier-coller et voir le résultat instantanément dans son navigateur. 


[wikipedia]: http://fr.wikipedia.org/wiki/
[responsivegridsystem]: http://www.responsivegridsystem.com/
[Brackets]: http://brackets.io/
[joelapompe]: http://www.joelapompe.net/