---
title: Prise en charge SVG
description: à compter de Windows 10 mise à jour anniversaire, Direct2D prend en charge les polices de couleur de rendu qui contiennent des contours de glyphe SVG, comme décrit dans la spécification OpenType (voir le tableau « SVG »).
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112514"
---
# <a name="svg-support"></a>Prise en charge SVG

à compter de Windows 10 mise à jour anniversaire, Direct2D prend en charge les [polices de couleur](../directwrite/color-fonts.md) de rendu qui contiennent des contours de glyphe SVG, comme décrit dans la [spécification OpenType](/typography/opentype/spec/) (voir [la table SVG](/typography/opentype/spec/svg)). à compter de Windows 10 Creators Update, Direct2D prend également en charge le rendu d’images SVG autonomes. Toutefois, certaines fonctionnalités SVG ne sont pas autorisées dans les polices OpenType SVG, et certaines fonctionnalités SVG ne sont actuellement pas prises en charge par Direct2D.  

cette rubrique identifie l’ensemble des fonctionnalités [SVG 1,1](https://www.w3.org/TR/SVG11/) prises en charge par Direct2D dans Windows 10 mise à jour anniversaire et versions ultérieures. Ce document s’applique à SVG dans les polices OpenType, ainsi qu’aux images SVG autonomes.

## <a name="supported-svg-elements-and-attributes"></a>Attributs et éléments SVG pris en charge

Direct2D prend en charge le rendu des éléments SVG suivants et des attributs associés pour chaque élément. D’autres éléments et attributs réguliers sont ignorés.



| Élément                                                                                  | Attributs standard pris en charge                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [cercle](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | ID, style, transformation, CX, CY, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | ID, style, transformation, clipPathUnits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | ID, style, transformation                                                                     |
| [DESC](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [ellipse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | ID, style, transformation, CX, CY, RX, Ry                                                     |
| [activée](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | ID, style, transformation                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | ID, style, transformer, x, y, largeur, hauteur, preserveAspectRatio, xlink : href               |
| [spline](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | ID, style, transformer, x1, y1, x2, Y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | ID, style, x1, y1, x2, Y2, gradientUnits, gradientTransform, spreadMethod, xlink : href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | ID, style, transformer, d                                                                  |
| [Polygone](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | ID, style, transformation, points                                                             |
| [polyligne](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | ID, style, transformation, points                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | ID, style, CX, CY, r, FX, FY, gradientUnits, gradientTransform, spreadMethod, xlink : href |
| [rectangulaire](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | ID, style, transformer, x, y, largeur, hauteur, RX, Ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | ID, style, décalage                                                                        |
| [svg](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | ID, style, x, y, largeur, hauteur, viewBox, preserveAspectRatio                             |
| [bonhomme](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | ID, style, transformer, x, y, largeur, hauteur, xlink : href                                    |



 

<sup>\*</sup>pris en charge uniquement dans Windows 10 Creators Update et versions ultérieures

## <a name="supported-svg-presentation-attributes"></a>Attributs de présentation SVG pris en charge

Direct2D prend également en charge les attributs de présentation suivants. Elles peuvent être spécifiées sur n’importe quel élément SVG, mais elles affectent uniquement l’apparence de certains éléments, comme décrit dans la spécification SVG (consultez [attributs de présentation](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   clip-chemin
-   clip-règle
-   color
-   vidéo<sup>\*</sup>
-   fill
-   opacité de remplissage
-   remplir-règle
-   opacity
-   dépassement de capacité
-   couleur d’arrêt
-   arrêter-opacité
-   stroke
-   Stroke-dashArray
-   Stroke-DashOffset
-   Stroke-LineCap
-   Stroke-LineJoin
-   Stroke-MiterLimit
-   trait-opacité
-   largeur du trait
-   vue<sup>\*</sup>

<sup>\*</sup>pris en charge uniquement dans Windows 10 Creators Update et versions ultérieures

## <a name="unsupported-svg-features"></a>Fonctionnalités SVG non prises en charge

### <a name="unsupported-elements-and-attributes"></a>Éléments et attributs non pris en charge

Tout élément ou attribut qui n’est pas inclus dans les listes ci-dessus est considéré comme non pris en charge par Direct2D. Lors de l’analyse du contenu SVG qui contient un attribut ou un élément non pris en charge, l’entité non prise en charge est ignorée. Le reste du contenu est rendu aussi fidèlement que possible.

### <a name="unsupported-length-units"></a>Unités de longueur non prises en charge

à partir de Windows 10 mise à jour anniversaire, Direct2D prend en charge uniquement les valeurs de longueur des espaces utilisateur et les valeurs de pourcentage de longueur. Les longueurs avec des suffixes d’unité, comme « mm » ou « em », ne sont pas prises en charge.

à partir de Windows 10 Fall Creators Update, Direct2D prend également en charge les identificateurs d’unité absolus : px, pt, pc, cm, mm et in. Les identificateurs d’unité relative (EM, ex) ne sont pas pris en charge.

### <a name="unsupported-image-sources"></a>Sources d’image non prises en charge

L’élément image est pris en charge uniquement si son attribut xlink : href a la valeur d’une image encodée en base64. Les références distantes ne sont pas prises en charge.

 

 