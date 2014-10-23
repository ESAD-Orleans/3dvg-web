---
layout: post
title:  "Insérer des images"
date:   2014-10-23 09:45:00
categories: html
tags: html image img

---


## Images pour le web

Il existe plusieurs moyen d’insérer des images sur une page web,
et il existe plusieurs types/formats d’image utilisable sur une page web.
Quatres types d’images sont autorisés, trois de types bitmap :

- JPEG
- PNG
- GIF

et un de type vectoriel :

- SVG

Nous verrons dans un prochain cours comment optimiser les images
afin qu’elles pèsent le moins lourd possible en préservant leur qualité.
En effet, le facteur *poids* est très important sur le web car de lui
dépend la vitesse de téléchargement d'une page.

## Enregistrer pour le web

Depuis Photoshop® ou Illustrator®, vous pouvez exporter vos images vers des formats web, en utilisant la commande
**Fichier > Enregistrer pour le Web**, commande `⌥⇧⌘S`

<img alt="save for web" src="/3dvg-web/images/save-for-web-interface.png" />

Nous reviendrons sur les différentes optimisations et formats dans une prochaine leçon.
Une chose reste néanmoins importante lors de l’enregistrement du **fichier image**, c’est son **dossier de destination**.
En effet, pour pouvoir utiliser l'image dans la page, il faudra que son fichier soit *rangé* dans un dossier *voisin* de la page web.
En général on utilise des dossiers spécifiques pour ranger toutes les images, afin de ne pas mélanger celles-ci avec le reste des fichiers HTML et CSS.

Dans notre projet, je vous propose de créer un dossier `images` et de l’enregistrer à l’intérieur.

Lors de l’enregistrement pour le Web, si vous tentez de nommer votre fichier avec des caractères spéciaux ou des espaces,
Photoshop® ou Illustrator® vous les convertira automatiquement en caractère de base.
Il est en effet peu recommandé — et donc **interdit — d’utiliser des caractères spéciaux** et des espaces dans les noms de fichier, globalement, sur le web



## La balise image : `img`


Le moyen le plus simple d’ajouter une image dans la page est d’utiliser la balise `img`.
La balise `img` est une balise orpheline, et possède deux attributs obligatoires `src` et `alt`
On doit saisir le chemin vers le fichier image dans l’attribut `src`.

{% highlight HTML %}

<img src="mon_dossier/mon_image.jpg" alt="mon image pour le web" />
{% endhighlight %}

Dans les recommandations HTML5, l’attribut `alt` est obligatoire pour la balise `img`.
Il sert à décrire l’image — pour les systèmes d’audio-description et les navigateurs sans image.

On reconnait dans l’exemple que j'ai utilisé un **chemin** d’une image **dans un dossier**.
Comme vu au dessus, je vous recommande de ranger toutes vos images dans un dossier.
Dans la notation des **chemins de fichier**, on écrit la hiérarchie des dossiers en les séparant par des `/` (**slash**)

	mon_dossier/un_autre/encore_un/mon_fichier.jpg

Une fois ajouté dans le code HTML, la balise `img` affiche l’image à 100%. Il est possible de forcer une taille pour cette image,
en utilisant les attributs `width` (largeur) et `height` (hauteur). Par défaut, on exprime ces tailles en pixels.

{% highlight HTML %}
<img src="mon_dossier/mon_image.jpg" width="400" height="200" alt="mon image pour le web" />
{% endhighlight %}

## Image css, en arrière-plan : `background`

L’autre moyen d’afficher une image est de l’ajouter en arrière-plan d’un bloc HTML, d’une balise.
Pour cela on utilise la propriété CSS `background` ou plus précisément `background-image`.
Pour décrire le **chemin** vers l’image on doit l’entourer du mot-clé `url("")`.

{% highlight HTML %}

<div class="decor">
	du texte informatif
</div>

{% endhighlight %}

{% highlight CSS %}

.decor{
	background-image:url("images/pattern.png");
/* autres propiétés du bloc */
	width: 100%;
	height: 200px;
	font-size: 30px;
	color: #fff;
	font-family: sans-serif;
	text-shadow: #10ff87 0 0 5px;
}
{% endhighlight %}

<img src="/3dvg-web/images/background-image-pattern.png" alt="background-image pattern" />

On voit que le comportement est différent de celui de la balise `img`.
En effet l’image est répétée et coupée au dimension du bloc, et du contenu texte de la balise est affiché sur l’image.




