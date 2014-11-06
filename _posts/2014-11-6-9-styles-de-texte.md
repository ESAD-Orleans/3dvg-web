---
layout: post
title:  "Styles de texte"
date:   2014-11-06 09:45:00
categories: css
tags: css texte typo

---

Le web est par nature — on l’a vu — textuel, hypertextuel. Il est donc naturel de se pencher sur la mise en place des styles sur le texte

## Les caractères

Voici une liste des propriétés CSS modifiant les caractères en eux-même. On verra ensuite comment modifier les espaces typographiques.

### `color` : couleur

{% highlight CSS %}color: #f99900; {% endhighlight %}

### `font-size` : taille

{% highlight CSS %}font-size: 12px; {% endhighlight %}
Il représente la hauteur d’un `em` — ou cadratin, la hauteur de M.

### `font-family` : famille

{% highlight CSS %}font-family: "Helvetica", "Arial", sans-serif; {% endhighlight %}

On peut mettre plusieurs nom de polices les un après les autres. Cela sert à utiliser des polices de substitution,
si les polices de rang un ne sont pas disponibles.
Nous verront plus tard comment installer une Google® Font sur une page web.

### `font-weight` : graisse

### `font-style` : italique

### `font-variant` : petites capitales

### `font-stretch` : étirement

{% highlight CSS %}
font-weight: bold;
font-style: italic;
font-variant: small-caps;
font-stretch: condensed;
{% endhighlight %}

On peut utiliser plusieurs type de graisse, mais celles-ci doivent
être disponible dans la police utilisée. À défaut, un **faux gras** peut-être appliqué, ce qui est mauvais.

{% highlight CSS %}
font-weight: bold;
font-weight: 100;
font-weight: 900;
{% endhighlight %}

Les graisses sont soit exprimées en mot, comme `strong` ou `normal`, soit en valeur numérique.
Les seules valeurs numériques acceptées sont `100, 200, 300, 400, 500, 600, 700, 800, 900`.
`100` correspond à *thin* et *black*, `normal` équivalent `500`.
On peut aussi utiliser des valeurs de graisse relative `stronger` et `lighter`.

`font-style` gère principalement l’italique, `font-stretch` le type d’étirement et `font-variant` les petites capitales.
Comme pour la graisse, Elle doit être disponible dans la police utilisée.
On se sert rarement de `font-stretch` car rarement disponible.

### `text-transform` : capitale ou bas-de-casse
{% highlight CSS %}
text-transform: uppercase; /* FORCE LES CAPITALES */
text-transform: lowercase; /* force les bas-de-casse */
text-transform: capitalize; /* Force Les Capitales En Début De Mot */
{% endhighlight %}

Ces styles forceront l’éditeur à respecter la charte graphique.

### `text-shadow` : ombre portée
{% highlight CSS %}text-shadow: blue 10px 10px 20px{% endhighlight %}
Sert à mettre une ombre portée, d’une certaine **couleur**, à un certain décallage **en x** et **en y**, avec un certain **flou**.
Toutes ces options sont séparées par des espaces.

Cette propriétée — *associée à texte transparent* — permet un **flou** sur une typographie.
{% highlight CSS %}text-shadow: black 0 0 5px;
color: transparent;{% endhighlight %}
<img src="/3dvg-web/images/text-shadow-blur.png" alt="text blur" width="124" />

### `text-decoration` : souligné
{% highlight CSS %}text-decoration:underline{% endhighlight %}
Souligne le texte. On peut aussi le barré avec `line-through` ou le sur-ligné avec `overline`. Par défaut, c'est la couleur du texte qui est utilisée.









