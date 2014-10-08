---
layout: post
title:  "Entête du document HTML"
date:   2014-10-09 09:45:00
categories: html
tags: html World-Wide-Web html5 balises hypertext
---


à l'intérieur de HEAD
---

\<meta charset="UTF-8" />
----

c’est la balise d’encodage. une chose un peu compliqué, mais qui sert à décrire les nombreuses variante d’écriture du monde. pour faire simple, utilisez l’encodage UTF-8, il temps à devenir la norme, car il couvre toutes les écritures. Cette balise `<meta />` est la première à insérer dans le head, car d’elle dépend tous le traitement du texte.

	<meta charset="utf-8" />

\<title>\</title>
----

c’est la balise de titre. Le titre d'un document HTML est très important, même si à la base, il est visiblement peu présent. le code suivant `<title>Mon exercice</title>`

![title tag.png](/3dvg-web/images/title_tag.png)

s’affiche dans l’onglet ou le titre de la fenêtre.
Il a une grande importance sémantique, puisque par exemple, c'est lui que **référence google**

![title google](/3dvg-web/images/title_google.png)

ici en bleu souligné.

\<link> pour attacher une feuille de style
----

quand on veut attacher une feuille de style `CSS` à la page HTML, on devra passer par cette balise et préciser le fichier .css que l'on veut utiliser

{% highlight HTML %}
<link href="styles/ma-feuille-de-styles.css" rel="stylesheet" />
{% endhighlight %}


[wikipedia]: http://fr.wikipedia.org/wiki/
[World_Wide_Web]: http://fr.wikipedia.org/wiki/World_Wide_Web
[Brackets]: http://brackets.io/
[joelapompe]: http://www.joelapompe.net/