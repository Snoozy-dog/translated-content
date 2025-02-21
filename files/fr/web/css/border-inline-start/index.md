---
title: border-inline-start
slug: Web/CSS/border-inline-start
tags:
  - CSS
  - Experimental
  - Propriété
  - Propriété logique
  - Reference
translation_of: Web/CSS/border-inline-start
---
{{CSSRef}}{{SeeCompatTable}}

La propriété** `border-inline-start`** est une propriété raccourcie qui permet de définir la bordure d'un élément pour le côté correspondant au début de l'élément dans le sens de lecture. Elle peut être utilisée pour définir les valeurs de {{cssxref("border-inline-start-width")}}, {{cssxref("border-inline-start-style")}} et {{cssxref("border-inline-start-color")}}.

{{EmbedInteractiveExample("pages/css/border-inline-start.html")}}

Cette propriété logique correspond à l'une des propriété physique équivalente selon le mode d'écriture, la directionnalité et l'orientation du texte. Autrement dit, elle correspond à l'une des propriétés {{cssxref("border-top")}}, {{cssxref("border-right")}}, {{cssxref("border-bottom")}} ou {{cssxref("border-left")}} selon les valeurs utilisées pour {{cssxref("writing-mode")}}, {{cssxref("direction")}} et {{cssxref("text-orientation")}}.

On peut rapprocher cette propriété des autres propriétés logiques raccourcies définissant les bordures des autres côtés :

- {{cssxref("border-block-start")}},
- {{cssxref("border-block-end")}},
- {{cssxref("border-inline-end")}}.

## Syntaxe

```css
border-inline-start: 1px;
border-inline-start: 2px dotted;
border-inline-start: medium dashed green;
```

### Valeurs

Une ou plusieurs valeurs parmi les suivantes, dans n'importe quel ordre :

- `<'border-width'>`
  - : La largeur de la bordure, voir {{cssxref("border-width")}}.
- `<'border-style'>`
  - : Le style utilisé pour la ligne de la bordure sur ce côté, voir {{cssxref("border-style")}}.
- `<'color'>`
  - : La couleur utilisé pour la bordure sur ce côté, voir {{cssxref("color")}}.

### Syntaxe formelle

{{csssyntax}}

## Exemples

### CSS

```css
div {
  background-color: yellow;
  width: 120px;
  height: 120px;
}

.exemple {
  writing-mode: vertical-rl;
  border-inline-start: 5px dashed blue;
}
```

### HTML

```html
<div>
  <p class="exemple">Texte d'exemple</p>
</div>
```

### Résultat

{{EmbedLiveSample("Exemples", 140, 140)}}

## Spécifications

| Spécification                                                                                                                | État                                             | Commentaires         |
| ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | -------------------- |
| {{SpecName("CSS Logical Properties", "#propdef-border-inline-start", "border-inline-start")}} | {{Spec2("CSS Logical Properties")}} | Définition initiale. |

{{cssinfo}}

## Compatibilité des navigateurs

{{Compat("css.properties.border-inline-start")}}

## Voir aussi

- Les propriétés physiques correspondantes :

  - {{cssxref("border-top")}},
  - {{cssxref("border-right")}},
  - {{cssxref("border-bottom")}},
  - {{cssxref("border-left")}}

- {{cssxref("writing-mode")}}, {{cssxref("direction")}}, {{cssxref("text-orientation")}}
