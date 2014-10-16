---
layout: post
title:  "Structure et syntaxe HTML"
date:   2014-10-16 09:45:00
categories: html
tags: html html5 balises espaces
---


## Les espaces, tabulation et retours à la ligne

Une chose importante, déjà : **Les espaces**.

le HTML est insensible au *espaces multiples, tabulations et retours à la ligne*.
ainsi, le texte HTML suivant

			Longtemps,
		je  me        suis

		couché
	de        bonne         heure.

s’affichera de cette manière dans le navigateur

	Longtemps, je me suis couché de bonne heure.

profitant de cela, on se servira des espaces, tabulations et des retours à la ligne, pour conserver la lisibilité du code.
Aussi, pour assurer des retours à la ligne, on utilisera la balise orpheline `<br/>`. Pour forcer une espace, on utilisera le **code html** `&nbsp;` (**n**o **b**reak **sp**ace)

## Les balises (tags)

En HTML, pour décrire le contenu, on utilise des balises (tags).

Chacune de ces balises ont un rôle particulier, qu’il faudra respecter.

## les deux formes de balises

il existe deux type de balise, les balises **en paires** et les balises **orphelines**.

les **balises paires** englobe du texte et peuvent contenir d’autres balises.

On écrit une balise ouvrante `<balise>` et une balise fermante `</balise>`

	<p>
		un exemple de paragraphe de texte
	</p>

les **balises orphelines** servent à insérer un élément à un endroit précis,
comme une image ou un retour à la ligne `<balise />`.

	<br /> ceci est un retour à la ligne

les attributs (attributes)
----

la plupart des balises possède des options, que l’on nomme **attribut**.
on note les attributs d'une balise de cette manière `<balise attribut=""></balise>`.

Pour les balises orpheline, la syntaxe est la même `<balise attribut="" />`.

Les balises peuvent avoir plusieurs attributs, certains sont obligatoires, d’autres sont facultatifs, on les notera de cette manière `<div id="exemple" class="classe"></div>`

## le commentaire

comme dans beaucoup de langage informatique, le HTML permet d'inclure des commentaires dans le code, qui seront invisible à l'interprétation. Ces commentaires permettent d'insérer de remarques cachées, ou d’isoler du code HTML temporairement sans le supprimer. la notation du commentaire est aussi une paire ovrante `<!--` et fermante `-->`. Tous le texte situé entre ces deux balise sera ignorée.

{% highlight HTML %}

du texte visible
<!-- un commentaire invisible -->
un autre texte visible <!-- et un autre commentaire
avec <span>du code ignoré</span>
-->

{% endhighlight %}

## des balises imbriquées

le langage HTML repose sur une imbrication de balise (hérité du XML). On l’a vu la vu précédement, les balise paires permettent d’inclure du texte. Elle permettent en outre d'inclure des balises. on parlera de balise **enfant/parent** et d’**arborescence** pour décrire cela

{% highlight XML %}

<racine>
	<parent>
		<enfant></enfant>
		<enfant>
			<petit />
			<petit />
			<petit />
		</enfant>
	</parent>
	<autre>
		<machin>
			<bidule />
		</machin>
		<chose />
		<truc />
	</autre>
</racine>

{% endhighlight %}

avec des vraies balises HTML, ça ressemble à ça

{% highlight HTML %}

<html>
	<head>
		<title>le titre</title>
	</head>
	<body>
		<div>
			<h1>un exemple réel</h1>
			<p>
				de paragraphe avec
				<b>du texte gras</b>
				et de
				<i>l’italique</i>
			</p>
		</div>
	</body>
</html>

{% endhighlight %}

## Structure du document HTML

Le HTML possède une structure minimum, un squelette obligatoire au bon fonctionnement de la page.

On va essayer de la décrire rapidement.

### <!doctype HTML>

Cette balise est spéciale, elle intervient toujours en début de document, elle est orpheline. Elle décrit le type de document HTML. si vous l'oubliez, la page sera chargé, mais le navigateur ne connaitra pas la norme HTML que vous utilisé (HTML5, XHTML, HTML4…) et utilisera une valeur par default. Le doctype pour HTML5 est assez simple c’est `<!doctype html>`

### <html>\</html>

C’est la balise racine (parente de toutes) les autres. elle contiendra toujours et seulement deux autres, `<head></head>` (l'entête de document) et `<body></body>` (le corps de document)

### \<head>\</head>

C’est la balise d’entête, qui contient les informations générales sur la page comme le titre, l'encodage, les meta. On y déclarera aussi des liaisons vers les feuilles de style CSS et les script JavaScript.

### \<body>\</body>

C’est la balise de corps, qui concerne donc la partie principale — visible — du contenu.

## exemple de structure minimum

Étant donné qu’un fichier HTML doit comporté certaines balises de manières obligatoire (c’est le cas pour le `doctype`, `html`, `head`, `body`, `title`)
on peut rapidement imaginer le code HTML minimum pour commencer, le voici : 

{% highlight HTML %}

<!doctype HTML>
<html>
	<head>
        <meta charset="utf-8" />
		<title>document sans titre</title>
	</head>
	<body>
	</body>
</html>

{% endhighlight %}

Dans cet exemple, on voit apparaitre une balise non décrite précédement. On peut la concidérer comme obligatoire, et elle concerne le **jeu de caractères** (*charset* en anglais). Nous utiliserons toujours le jeu de caractère `utf-8`, le plus universel.