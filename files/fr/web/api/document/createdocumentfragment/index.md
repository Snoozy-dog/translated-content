---
title: document.createDocumentFragment
slug: Web/API/Document/createDocumentFragment
tags:
  - API
  - DOM
  - Document
  - HTML
  - Méthode
  - Reference
translation_of: Web/API/Document/createDocumentFragment
---
{{ApiRef("DOM")}}

Crée un nouvel objet vide de type {{domxref("DocumentFragment")}}.

## Syntaxe

    var fragment = document.createDocumentFragment();

`fragment` est une référence vers un objet vide de type {{domxref("DocumentFragment")}} .

## Description

Les objets `DocumentFragments` sont analogues à des nœuds du DOM, mais ne font jamais partie de l'arbre DOM. Le cas d'usage le plus courant consiste à créer un fragment pour y stocker des éléments, puis à ajouter en une seule opération le fragment à l'arbre DOM, ce qui a pour effet de le remplacer par tous ses éléments enfants.

Le principal avantage de cette méthode de mise à jour du DOM vient du fait que le fragment est stocké en mémoire, et pas dans l'arbre DOM lui-même, de sorte que le modifier ne déclenche pas de [reflow](http://code.google.com/speed/articles/reflow.html) (le calcul des positions et de la géométrie de chacun des éléments de la page affichée). Par conséquent, l´utilisation de fragments pour effectuer des mises à jour du DOM donne souvent lieu à une [amélioration des performance](http://ejohn.org/blog/dom-documentfragments/)s.

## Exemple

Cet exemple crée une liste des principaux navigateurs du web.

### HTML

```html
<ul id="ul">
</ul>
```

### JavaScript

```js
var element  = document.getElementById('ul'); // en supposant qu'ul existe
var fragment = document.createDocumentFragment();
var browsers = ['Firefox', 'Chrome', 'Opera',
    'Safari', 'Internet Explorer'];

browsers.forEach(function(browser) {
    var li = document.createElement('li');
    li.textContent = browser;
    fragment.appendChild(li);
});

element.appendChild(fragment);
```

### Résultat

{{EmbedLiveSample("Example", 600, 140)}}

## Spécification

| Spécification                                                                                                                            | Statut                           | Commentaire                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ------------------------------------------------ |
| {{SpecName('DOM WHATWG', '#dom-document-createdocumentfragment', 'Document.createDocumentFragment()')}} | {{Spec2('DOM WHATWG')}} | Définition initiale dans la spécification DOM 1. |

## Compatibilité des navigateurs

{{Compat("api.Document.createDocumentFragment")}}

## Voir aussi

- {{domxref("DOMImplementation.createDocument", "document.implementation.createDocument()")}}
- {{domxref("documentFragment")}}
