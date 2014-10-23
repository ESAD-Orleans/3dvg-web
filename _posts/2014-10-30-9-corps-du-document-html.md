---
layout: post
title:  "Corps du document HTML"
date:   2014-10-30 09:45:00
categories: html
tags: html World-Wide-Web html5 balises hypertext
---


à l’intérieur de BODY
---

la balise `<body></body>` est unique dans le document, elle englobe tout ce que l'utilisateur verra dans son navigateur.

organiser le texte
----
HTML est un langage de **texte**. Ce texte est organisé — **`sémantiquement`** — à l'intérieur de la balise `<body>`. L’organisation vise à décrire les différents niveaux et types d’informations dans la hiérarchie du document.

les paragraphes
----
la forme basique du traitement de texte est le paragraphe. c’est la balise `<p></p>`
par exemple :

{% highlight HTML %}
<p>
Un artiste qui possède à fond la théorie de son art,
et qui ne le cède à aucun autre dans la pratique,
m’a assuré que c’était par le tact
et non par la vue qu’il jugeait de la rondeur des pignons ;
qu’il les faisait rouler doucement entre le pouce et l’index,
et que c’était par l’impression successive
qu’il discernait de légères inégalités
qui échapperaient à son œil.
</p>

<p>
On m’a parlé d’un aveugle qui connaissait au toucher
quelle était la couleur des étoffes.
</p>
{% endhighlight %}
les titres
----
pour hiérarchiser ses paragraphes, il est possible d’ajouter des titres et des sous-titres. Les titres s’organisent en niveaux d’importance de 1 à 6. Dans les faits, on utilisent les balises de `h1` (titre principal du document) à `h6` (sous-titres de rang 6).

{% highlight HTML %}
<h1>Titre de la Page HTML</h1>
<h2>sous-titre important</h2>
<h4>sous-titre de moindre importance</h4>
{% endhighlight %}

ces niveaux permettent de décrire (notament à des fins algorithmiques) les concepts importants de votre document HTML. La balise `<h1></h1>`est très importante, il faut donc l’utiliser — car sa valeur est très forte — mais attention, il est préférable qu’elle soit présente ```une seule fois par page```. on place la balise `h1` au début du `body`, ou dans ses première ligne. Contrairement à `h1` les balises de niveaux inférieures `h2`, `h3`, `h4`, `h5` et `h6` seront en dessous, leurs répétitions et ordres n'ont pas d'importance.

mettre en valeur le texte
----
au sein d’un paragraphe, on peut mettre en valeur des mots, des groupes de mots, des phrases, etc… de nombreuses balises sont faites pour ça. c’est le cas de `em`, `strong`, `mark`, `i`, `b`, `u`…

Force : \<strong>\</strong>
----
c’est la balise de force, d’importance `<strong></strong>`, qui renforce un extrait du reste du texte. visuelement, par défault, cela se traduit par le gras. la vraie balise gras est la balise `b`.

	un extrait de texte <strong>avec</strong> une importance

Emphase : \<em>\</em>
----
c’est la balise d’emphase `<em></em>`, qui détache un extrait du reste du texte. visuelement, par défault, cela se traduit par l'italique. la vraie balise italique est la balise `i`.

{% highlight HTML %}
un extrait de texte <em>avec</em> une emphase
{% endhighlight %}

Graisse et italique : \<b>\</b> & \<i>\</i>
----
contrairement aux balises `strong` et `em`, les balises `b` (bold) et `i` (italic) n’ont pas de valeurs sémantiques. il est donc préférable de ne pas les utiliser, sauf si justement on ne veut pas distinguer de valeurs sémantiques.

{% highlight HTML %}
un extrait avec du <b>gras</b> de <i>l’italique</i>.
on peut les imbriquer pour faire du <b>gras <i>italique</i></b>
{% endhighlight %}

Souligné : \<u>\</u>
----
c’est la balise de soulignement `u` (underline).

{% highlight HTML %}
	un exemple <u>de soulignement</u>.
{% endhighlight %}

Barré : \<del>\</del>
----
c’est la balise pour barrer `del` (delete). Elle indique sémantiquement un contenu faux ou obsolète.

{% highlight HTML %}
	un exemple <del>de barré</del>.
{% endhighlight %}


Indice et exposant : \<sub>\</sub> & \<sup>\</sup>
----
ce sont les balises qui servent à placer une partie du texte en indice ou en exposant.

{% highlight HTML %}
	un exemple d’<sub>indice</sub> et d’<sup>exposant</sup>
{% endhighlight %}

Citations : \<blockquote>\</blockquote>
----
si vous avez à signifier une citation de texte, une balise existe pour cela, la balise `blockquote`. visuelement, par défault, elle se traduit par une tabulation.

{% highlight HTML %}
<blockquote>
    Maître Corbeau, sur un arbre perché,<br/>
    Tenait en son bec un fromage.<br/>
    Maître Renard, par l'odeur alléché,<br/>
    Lui tint à peu près ce langage :<br/>
    "Hé ! bonjour, Monsieur du Corbeau.<br/>
    Que vous êtes joli ! que vous me semblez beau !
</blockquote>
Jean de la Fontaine.
{% endhighlight %}

Préformaté et code : \<pre>\</pre>
----
la balise préformaté `pre` permet de conserver les espaces, les tabulations et les retours chariots.

{% highlight HTML %}
<pre>Un retour
à la ligne			et des tabulation</pre>
{% endhighlight %}

Code : \<code>\</code>
----
la balise code sert à afficher du code informatique. visuellement, par default, cela se traduit par l'utilisation de caractère à chasse fixe (mono-space).

{% highlight HTML %}
	<code> du <b>code</b> en gras. </code>
{% endhighlight %}

Listes : \<ul>\</ul> \<ol>\</ol> & \<li>\</li>
----
les balises de liste permettent d’ordonner du contenu, point par point, ligne par ligne. Il existe deux types de liste, les non-ordonnées `ul` et les ordonnées `ol`. Quelque soit ce type, chacun des **ligne** de la liste sera représenté par la balise `li`.

les listes non-ordonnées sont les plus fréquentes, et sont représentées visuelement par une suite de point à la ligne les uns les autres.

{% highlight HTML %}
Une liste d’animaux :
<ul>
	<li>Veaux</li>
	<li>Vaches</li>
	<li>Cochons</li>
</ul>
{% endhighlight %}

les listes ordonnées permettent d’ajouter une valeur numérale à la liste. un petit chiffre apparait devant eux

{% highlight HTML %}
Le plan parfait de rédaction
<ol>
	<li>thèse</li>
	<li>antithèse</li>
	<li>synthèse</li>
</ol>
{% endhighlight %}

les listes peuvent `s’imbriquer les unes dans les autres`, pour faire des hiérarchies. Par défault, visuelement, chaque niveau aura une tabulation. un exemple un peu plus long :

{% highlight HTML %}
<h1>La Cinquième République</h1>
<ul>
    <li><h2>Présidents de la République</h2>
        <ol>
            <li>De Gaulle
                <ul>
                    <li>1959-1962</li>
                    <li>1962-1968</li>
                    <li>1968-1969</li>
                </ul>
            </li>
            <li>Pompidou
                <ul>
                    <li>1969-1974</li>
                </ul>
            </li>
            <li>Giscard d’Estain
                <ul>
                    <li>1974-1981</li>
                </ul>
            </li>
            <li>Mitterand
                <ul>
                    <li>1981-1988</li>
                    <li>1988-1994</li>
                </ul>
            </li>
            <li>Chirac
                <ul>
                    <li>1995-2002</li>
                    <li>2002-2007</li>
                </ul>
            </li>
            <li>Sarkozy
                <ul>
                    <li>2007-2012</li>
                </ul>
            </li>
            <li>Hollande
                <ul>
                    <li>2012-Aujourd’hui</li>
                </ul>
            </li>
        </ol>
    </li>
    <li><h2>Premiers Ministres</h2>
        <ol>
            <li>Debré</li>
            <li>Pompidou</li>
            <li>Couve de Murville</li>
            <li>Chaban-Delmas</li>
            <li>Messmer</li>
            <li>Chirac</li>
            <li>Barre</li>
            <li>Morroy</li>
            <li>Fabius</li>
            <li>Chirac</li>
            <li>Rocard</li>
            <li>Cresson</li>
            <li>Bérégovoy</li>
            <li>Balladur</li>
            <li>Juppé</li>
            <li>Jospin</li>
            <li>De Villepin</li>
            <li>Fillion</li>
            <li>Ayrault</li>
        </ol>
    </li>
</ul>
{% endhighlight %}

Liens
----
Le HTML est un langage `hypertexte`, `hypertextuel`. Cela signifie qu’une page, un document HTML est pensé comme partie intégrante d’un système de fichier — typiquement en réseau, internet — et que des parties du texte sont reliés à d’autres contenus sur d’autres documents.
le terme vernaculaire pour l’hypertexte est le **lien**. en HTML, la balise pour marquer un lien est le `a` (anchor). Elle prend plusieurs attributs — certains obligatoires — que nous alons préciser.

	<a href="http://www.google.fr">lien vers Google</a>
le lien ci-dessus est un lien vers l’`URL` du site web de google, *www.google.fr*. on l’a précisé dans l’attribut `href`

	<a href="http://www.google.fr" target="_blank">lien vers Google</a>
à la différence du précédent exemple, j’ai utilisé l’attribut `target` avec pour valeur `_blank`. cette option permet d’ouvrir le lien dans une nouvelle fenêtre ou onglet.
dans l’exemple, on observe aussi que l’URL comporte le `protocole`, ici `HTTP` marqué par `http://`, il peut être `HTTPS` quand la connection est sécurisée `https://`. Préciser le protocole est obligatoire dans le href. l’oublier causera des erreurs et des `liens morts`.

URL absolue
----
les liens absolus sont des liens vers une `URL` absolue. Cela signifie que le chemin vers le fichier rédigé de manière complete. On s’en sert pour faire référence à des adresses Web autre que le site web courant
	<a href="http://www.google.fr">lien vers Google</a>

quand on travail un fichier HTML sur son ordinateur, le protocole utilisé est `file://` avec l’adresse du fichier sur le disque dur. c’est cette URL qui apparait dans la barre d’adresse du navigateur.

URL relative
----
les liens relatif sont des liens `relatif` à la page courante. cela permet de lié des fichiers qui sont dans les mêmes dossiers.

	<a href="contact.html">lien vers la page contact</a>

le lien ci-dessus ouvrira la page contact.html présente dans le même dossier que la page courante. utiliser des `URL relatives` permet de déplacer ses dossiers, d’uploader ses fichiers sur le serveur, sans `casser` les liens. on n’utilise pas de protocole dans ce cas, car c’est le protocole courant qui sera utilisé.

la notation d’URL utilise la **`syntaxe à points et slashs`**. Ainsi

- `.` (point) fait référence au dossier actuel.
- `..` (point-point) fait référence au dossier parent.
- `/` (slash) sépare les dossiers

ainsi, pour faire référence à un fichier dans le dossier parent, on utilise cette syntaxe. `../un_fichier.jpg`


URL ancre-nommées
----
les liens en `ancres` sont des liens interne au document HTML, il permet de faire défiler la page jusqu’à l’ancre-nommée. ainsi, dans un long document, les ancres pourront renvoyer aux notes en bas de page, et inversement, faire remonter une note vers son origine.
la syntaxe des ancres utilise le symbole dièse `#` dans l’URL. on peut utiliser les ancres au sein du document, mais aussi pour pointer à un endroit précis d’un autre document. `l’ancre-nommée` fait référence à un attribut `id` au sein d’une balise du document. exemple :

	<div style="height:1000px; background:turquoise; color:white;">
    un paragraphe avec <a id="ref1" href="#note1">une note<sup>1</sup></a> en bas de page
	et aussi <a id="ref2" href="#note2">une autre note<sup>2</sup></a>
	</div>
	<ul>
		<li id="note1">
			une explication de la note 1
			<a href="#ref1">retour au texte</a>
		</li>
		<li id="note2">
			une explication de la note 2
			<a href="#ref2">retour au texte</a>
		</li>
	</ul>

On peut faire pointer un lien vers l’ancre d’un document en absolue, ainsi :

	<a href="http://fr.wikipedia.org/wiki/HTML#Syntaxe_de_HTML">la syntaxe HTML</a>

le lien ci-dessus nous ramène directement au [paragraphe « Syntaxe de HTML »](http://fr.wikipedia.org/wiki/HTML#Syntaxe_de_HTML) de [l’article sur HTML](http://fr.wikipedia.org/wiki/HTML) de **Wikipedia**. Ainsi un lien en ancre-nommé peut servir au sein d'un document HTML, mais aussi pour des liens externes.

Images
----

on peut insérer des images avec la balise orpheline `img`. on précisera l’URL de l’image dans l’attribut obligatoire `src`

	<img src="mon_image.jpg" />

les navigateurs supportent à l’heure actuelle trois types d’images : `gif`,`jpg`,`png`. on peut aussi utiliser, dans certaines condition, le format vectoriel `svg`. Chaque format a son rôle et son utilité.
l’attribut src supporte les URL absolue et relative, qui marche de la même manière que les liens. Ainsi, je peux écrire :

	<img src="../un_dossier_image/une_image.png" />
	<img src="./un_autre_dossier/une_autre_image.png" />
	<img src="http://www.google.fr/images/srpr/logo4w.png" /> image depuis google.fr

si les URL de vos images sont cassées. un petit symbole apparaitra dans votre navigateur.


![x](img/img-fail.gif)


[wikipedia]: http://fr.wikipedia.org/wiki/
[World_Wide_Web]: http://fr.wikipedia.org/wiki/World_Wide_Web
[Brackets]: http://brackets.io/
[joelapompe]: http://www.joelapompe.net/