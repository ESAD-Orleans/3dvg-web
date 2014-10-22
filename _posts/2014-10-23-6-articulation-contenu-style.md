---
layout: post
title:  "Articulation contenu/style"
date:   2014-10-16 09:45:00
categories: html
tags: html css selecteurs

---


## séparation entre contenu et style

Les langages web HTML et CSS permettent de mettre en page des documents. On l’a déjà dit, le HTML permet de gérer l’aspect **sémantique** (le sens) et le CSS de gérer la **mise en forme**, éssentielement visuelle, graphique. On dit donc qu’il y a une séparation entre le contenu et le style, qui s’opère dans la pratique dans deux types de fichiers, le code HTML et le code CSS. 

Mais comme le style s’applique toujours à un contenu, ces deux langages ont des articulations — **des sélecteurs** — qui permettent d’appliquer **un style** à un **élement HTML**


## l’articulation HTML/CSS par l’exemple

Rien ne vaut un exemple pour rapidement comprendre la liaison entre HTML et CSS

{% highlight HTML %}
<div>
	<h3>Lorem ipsum</h3>
	<p>Le faux texte permet de remplir du paragraphe.</p>
	<p>Un second exemple</p>
</div>
{% endhighlight %}

{% highlight CSS %}
h3{
	color: #ff3300;
	text-decoration: underline;
}
p{
	line-height: 30px;
}
{% endhighlight %}

Dans l’exemple ci-dessus, c’est le selecteur CSS le plus simple qui est mis en place, le **selecteur d’élement**.
Dans le code CSS, on voit deux selecteurs, `h3` et `p` qui ciblent les balises (ou élements) éponymes en HTML,
les balises `<h3></h3>` et `<p></p>`. Ces deux selecteurs CSS possèdent ensuites des **propriétés** CSS — décritent en accolades `{` `}` —,
qui permettent de modifier l’aspect visuel. Ici c’est `color`, `text-decoration` et `line-height` qui permettent respectivement de
modifier *la couleur, le soulignement, et la hauteur de ligne*.

## les sélecteurs par identifiant : `#`

Les selecteurs d’élements ont une qualité … qui fait leur défaut : **il cible l’ensemble des balises du même nom**.
On arrive vite à un problème quand on veut appliquer différents style à des balises de même nom (comme une balise `div`, par exemple, qui revient très souvent)
On utilisera donc le **sélecteur par identifiant** (ou par **id**).

En CSS, on utilise le symbole `#` (**dieze**) pour comme **sélecteur d’identifiant**.

Voici un exemple d’utilisation d’**identifiant** sur 3 blocs.

{% highlight HTML %}
<div id="bloc-un"></div>

<div id="bloc-deux"></div>

<div id="bloc-trois"></div>
{% endhighlight %}

{% highlight CSS %}

#bloc-un{
	background:#ff99cc;
	width:200px;
	height:100px;
}

#bloc-deux{
	background:#0099ff;
	width:300px;
	height:50px;
}

#bloc-trois{
	background:#33ffcc;
	width:100px;
	height:75px;
}

{% endhighlight %}

Les trois selecteurs permettent ici de sélectionner les trois balises, qui ont un `attribut id` et d’appliquer des tailles et couleurs d’arrière-plan.

![bloc 123](/3dvg-web/images/blocs-123.png)

Le selecteur par **id** a cependant elle aussi un problème, car l’attribut **id** doit être unique à tout le document HTML.

## Les sélecteurs par classe : `.`

Voici donc le sélecteur intermédiaire entre celui d’*élement* (trop global) et celui d’*identifiant* : le sélecteur de **classe**. Il sera souvent le plus recommandé, car il a une *priorité moyenne* dans les priorités css (nous y reviendrons).

En CSS, on utilise le symbole `.` (**point**) pour comme **sélecteur de classe**.

{% highlight HTML %}
<div class="bleu">bleu</div>

<div class="vert">vert</div>

<div class="bleu souligne">bleu souligné</div>
{% endhighlight %}

{% highlight CSS %}

.bleu{
	color: #3355ff;
}
.vert{
	color: #55ff33;
}
.souligne{
	text-decoration: underline;
}

{% endhighlight %}

Et voici le résultat :

<img alt="class vert bleu souligné" src="/3dvg-web/images/class-bleu-vert-souligne.png" width="103" height="70" />

On observe que contrairement à **l’attribut** `id` qui est unique, plusieurs **classes** peuvent être utilisée.
On utilise **l’attribut** `class`, et si on veut utiliser plusieurs classes, on les **sépare par des espaces**.

## et d’autres (**pseudo-**)sélecteurs…

Il existe d’autres types de sélecteurs, que l’on nomme **pseudo-sélecteur**.
Certains permettent de décrire des positions dans la hiérarchie HTML, d’autres des états d‘interaction de la balise — comme le survol.

{% highlight CSS %}

:hover{
	/* le survol d’un élément le transforme en rouge */
	color: #f00;
}

{% endhighlight %}

Nous reviendrons plus tard sur ces nombreux pseudo-selecteurs, pseudo-classes et pseudo-éléments.


[wikipedia]: http://fr.wikipedia.org/wiki/
[responsivegridsystem]: http://www.responsivegridsystem.com/
[Brackets]: http://brackets.io/
[joelapompe]: http://www.joelapompe.net/