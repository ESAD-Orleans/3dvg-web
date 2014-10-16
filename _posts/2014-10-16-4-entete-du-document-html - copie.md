---
layout: post
title:  "Entête du document HTML"
date:   2014-10-16 09:45:00
categories: html
tags: html World-Wide-Web html5 balises hypertext
---


## à l'intérieur de HEAD

### \<meta charset="UTF-8" />

C’est la balise d’**encodage** du texte, des caractères. L’encodage est une chose assez complexe, et sert à décrire les nombreuses variante d’écriture du monde sous forme numérique, et donc obligatoire. 

Pour faire simple, utilisez l’encodage `UTF-8`, il est la norme, car il couvre toutes les écritures du monde, alphabétiques et idéogrammatiques. 

Cette balise `<meta />` est donc la première à insérer dans le head, car d’elle dépend tous le traitement du texte.

	<meta charset="utf-8" />

### \<title>\</title>

c’est la balise de **titre**. Le titre d'un document HTML est très important, même si à la base, il est visiblement peu présent. le code suivant `<title>Mon exercice</title>`

![title tag.png](/3dvg-web/images/title_tag.png)

s’affiche dans l’onglet ou le titre de la fenêtre.
Il a une grande importance sémantique, puisque par exemple, c'est lui que **référence google**

![title google](/3dvg-web/images/title_google.png)

ici en bleu souligné.

\<link> pour attacher une feuille de style
----

Quand on veut attacher une feuille de style `CSS` à la page HTML, on devra passer par cette balise et préciser le fichier .css que l'on veut utiliser

{% highlight HTML %}
<link href="styles/ma-feuille-de-styles.css" rel="stylesheet" />
{% endhighlight %}

Il est possible d'attacher autant de feuille de style que l'on veut par page. 

Le fait de pouvoir séparer dans un fichier CSS les styles (la mise en forme) du contenu (le sens) permet de mutualiser les feuilles de style d'une page à une autre. Ainsi, pour un site web, on aura les même feuilles de style pour toutes les pages. 

\<script> pour attacher du javascript
----

Même si nous ne le verrons pas directement ce semestre, la balise script permet d'attacher au document un script externe, qui sera exécuté. 
les rôles de ses script `javascript` peuvent être très varié, plus ou moins complexe. Il servent à faire par exemple, des interactions dynamiques, des modification en direct du contenu de la page.

{% highlight HTML %}
<script src="js/mon-fichier.js" type="text/javascript"></script>
{% endhighlight %}


[wikipedia]: http://fr.wikipedia.org/wiki/
[World_Wide_Web]: http://fr.wikipedia.org/wiki/World_Wide_Web
[Brackets]: http://brackets.io/
[joelapompe]: http://www.joelapompe.net/