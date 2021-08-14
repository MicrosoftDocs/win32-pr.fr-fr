---
title: Types VML de base
description: cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Migrez les pages Web et les applications qui reposent sur VML sur SVG ou sur d’autres normes largement prises en charge.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Langage VML (VML), types de base
- VML (langage VML), types de base
- graphiques vectoriels, types VML de base
- Langage VML (VML), types
- VML (langage VML), types
- graphiques vectoriels, types VML
- types VML de base
- type booléen
- type de fraction
- type ordonné
- type de longueur
- type de mesure
- type d’angle
- type de couleur
- type de police
- type de bitmap
- Type vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dbb2e540e809b88b446cceda9973f8988c7241cae7f4f96402a0edc7906550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347774"
---
# <a name="basic-vml-types"></a>Types VML de base

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

**Contents**

-   [Introduction](#introduction)
-   [boolean](#boolean)
-   [fraction](#fraction)
-   [ordonnée](#ordinate)
-   [length](#length)
    -   [Autres représentations](#alternative-representations)
-   [unité](#measure)
    -   [Autres représentations](#alternative-representations)
-   [angle](#angle)
    -   [Autres représentations](#alternative-representations)
-   [color](#color)
    -   [Unités de couleur](#color-units)
    -   [Couleurs HTML](#html-colors)
    -   [Couleurs du schéma](#scheme-colors)
    -   [Couleurs système](#system-colors)
    -   [Couleurs pures](#pure-colors)
    -   [Réglages des couleurs](#color-adjustments)
-   [son](#font)
-   [bitmap](#bitmap)
    -   [Formats de fichiers image](#picture-file-formats)
-   [graphiques](#vector)

## <a name="introduction"></a>Introduction

Cette proposition utilise un petit nombre de types de base, listés dans le tableau ci-dessous.



| Type                  | Élément           | Représentation fondamentale | Description                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [boolean](#boolean)   |                   | 1 bit                      | Valeur booléenne : true ou false.                                                                      |
| [fraction](#fraction) |                   | Numéro 2 6                 | Valeur numérique, mise à l’échelle par 2 6 (65536) et stockée en tant qu’entier signé.                               |
| [ordonnée](#ordinate) |                   | signe plus (+) de 30 bits   | Une partie d’une coordonnée (par exemple, dans un chemin d’accès), les valeurs définies par Coord.                                |
| [length](#length)     |                   | [UME](#length)             | Longueur physique, telle que la largeur d’une ligne ou la taille d’une police.                                |
| [unité](#measure)   |                   | UME ou numéro 2 6          | Soit une longueur physique, notamment un nombre de pixels de l’appareil, soit une fraction d’une autre quantité. |
| [angle](#angle)       |                   | degrés 2 6                | Angle ; positif dans le sens des aiguilles d’une montre.                                                                     |
| [color](#color)       | [c](#color)       | complex                    | Élément qui autorise la dérivation d’une couleur.                                                        |
| [son](#font)         | [son](#font)     | complex                    | Description d’une police.                                                                             |
| [bitmap](#bitmap)     | [bitmap](#bitmap) | href                       | Référence à un fichier image externe.                                                             |
| [graphiques](#vector)     | [v](#vector)      | complex                    | Description d’un tracé de vecteur                                                                       |



 

La « représentation fondamentale » est la représentation de précision la plus élevée que la proposition requiert une implémentation conforme pour tenir à jour ; les données seront perdues si l’implémentation n’est pas en mesure de représenter les données dans la précision requise. Les types de couleur, de police et de vecteur correspondent à des éléments qui ont eux-mêmes une structure, ce qui n’est pas le type de base ; Toutefois, il est pratique de les traiter en tant que tels dans le cadre de cette proposition.

Chaque type de base non complexe a un élément associé du même nom. Ces noms d’éléments sont réservés et ne peuvent pas être utilisés à d’autres fins dans les extensions, même si l’utilisation se trouve dans un élément d’extension OnView = "Skip". Pour cette raison, il est possible pour une implémentation qui rencontre des données XML inconnues de fournir un stockage interne efficace du code XML inconnu tant que les valeurs sont placées dans les éléments « type ».


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



Dans le premier exemple ci-dessus, la chaîne « 1,578 » doit être stockée sous la forme d’une séquence de caractères (l’implémentation ne sait pas s’il s’agit d’une chaîne ou d’un nombre); dans le deuxième exemple, l’élément fraction indique que le contenu est un nombre, il peut donc être converti en représentation de fraction haute précision.

Les types complexes (y compris les bitmaps) ont des noms d’éléments associés qui sont utilisés pour délimiter la valeur. Cela simplifie l’analyse en s’assurant que les tâches d’analyse plus complexes sont associées à des balises d’éléments uniques.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="boolean"></a>boolean


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



Une valeur booléenne est représentée sous la forme d’un mot clé qui indique l’état de l’indicateur. Les mots clés suivants sont définis.



| Valeur pour true | Valeur pour false |
|----------------|-----------------|
| true           | false           |
| oui            | non              |
| sur             | arrêt             |
| t              | f               |
| 1              | 0               |



 

Une implémentation peut écrire n’importe quelle valeur et doit reconnaître toutes les valeurs. Une implémentation est libre de modifier les valeurs d’une représentation à une autre.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="fraction"></a>fraction


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



Toutes les valeurs numériques (c’est-à-dire, les valeurs de quantités sans dimension) de cette proposition peuvent être stockées sous forme d’entiers en les mettant à l’échelle de 2 6 (65536). Un nombre peut être donné dans ce formulaire, avec le suffixe f ou en tant que nombre décimal sans suffixe. Ainsi, les éléments hypothétiques suivants représentent la même valeur.


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



Une quantité avec le suffixe f doit être un nombre entier ; les nombres fractionnaires ne sont pas autorisés. L’entier résultant doit être représenté comme un nombre signé de complément 32 bits 2. par conséquent, la plage effective de la représentation est 32768 (en fait, inférieure à 32768 et supérieure ou égale à-32768).

Une implémentation conforme est requise pour conserver les valeurs exprimées sous forme de valeurs f. Les valeurs représentées sous forme de nombres décimaux peuvent être converties en une valeur f et stockées de cette façon. Une application est autorisée à enregistrer des valeurs générées en interne dans toute unité appropriée ; Toutefois, une valeur lue à partir d’un document existant doit être maintenue à la précision d’origine complète ou doit être convertie en valeur f.

Si l’implémentation ne parvient pas à effectuer cette opération, il doit avertir l’utilisateur que des données peuvent être perdues. (Il est possible d’émettre un tel avertissement une fois lorsque des données générées en externe sont rencontrées pour la première fois.)

Quand une valeur décimale est convertie au format f, l’implémentation peut utiliser n’importe quel mode d’arrondi arithmétique ; Toutefois, un nombre entier doit être converti au format f exactement. Il est recommandé que les implémentations soient converties par un arrondi à moins l’infini et que la conversion soit toujours exacte.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="ordinate"></a>ordonnée


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



Les unités du système de coordonnées établi par le repère sont d’un type nominal, appelé ordonnée. Il s’agit d’une mesure de longueur, mais elle est utilisée uniquement par rapport au rectangle établi par Coord. Toute valeur de type ordonné est mise à l’échelle en fonction des valeurs *w* et *h* du repère et du rapport résultant utilisé pour établir une mesure réelle sur le périphérique de sortie.

Une implémentation conforme doit pouvoir gérer des valeurs ordonnées allant jusqu’à 30 bits plus le signe (c’est-à-dire un entier signé de 31 bits, et non un entier signé 32 bits). Toutefois, il est recommandé que les implémentations tentent de produire des coordonnées pour le chemin d’accès et des éléments similaires qui ont environ 16 bits de précision. Cela réduira le risque de dépassement de capacité négatif ou de dépassement de capacité dans une implémentation non conforme.

les valeurs ordonnées sont toujours intégrales. Une virgule décimale ne peut pas apparaître dans une valeur de type ordonnée. Aucun spécificateur d’unité ne peut être ajouté aux valeurs de type ordonnée.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="length"></a>length


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



Une longueur est une mesure du monde réel ou, parfois, une mesure en pixels de périphérique. Il est recommandé que les implémentations évitent l’utilisation de pixels de périphérique (PX).

Tous les qualificateurs d’unités [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) standard sont autorisés sur une longueur. En outre, le qualificateur u.m.e. peut être utilisé. Ce qualificateur fait référence à une unité (l’unité de mesure anglaise), qui est un dénominateur commun des quantités de mesure dans un usage répandu dans les graphiques informatiques. L’UEM est de <sup>pouce</sup> /914400, c’est-à-dire qu’il y a 914400 UME par pouce. Le tableau suivant répertorie le nombre d’Emu dans un petit nombre d’unités couramment rencontrées.



| Nombre d’EMU | Nombre par pouce | Nombre par millimètre | Description             |
|----------------|-----------------|-----------------------|-------------------------|
| 360            |                 | 0,01                  | HIMETRIC Win32          |
| 12700          | 72              |                       | point                 |
| 635            | 1440            |                       | TWIP Win32              |
| 762            | 1200            |                       | Imprimante haute résolution |



 

Les nombres fractionnaires de EMU ne sont pas autorisés. Toute mesure doit être représentée en tant que nombre entier signé 32 bits d’EMU, ce qui limite l’amplitude d’une mesure à 2348 pouces environ 59 mètres ou 65 mètres. Étant donné que les mesures font toujours référence à la taille d’un rendu sur un appareil de sortie à écran ou page nominal, elles se trouvent toujours dans cette plage.

Notez, toutefois, que la représentation n’est pas appropriée pour les mesures du monde réel et que, lorsque celles-ci sont enregistrées (par exemple, pour enregistrer la taille réelle d’un chemin d’accès), une autre représentation doit être utilisée.

Une implémentation conforme est requise pour conserver les valeurs qui sont des nombres exacts de EMU. Les valeurs représentées d’une autre manière peuvent être converties en une valeur UME et stockées de cette façon. Une application est autorisée à enregistrer des valeurs générées en interne dans toute unité appropriée ; Toutefois, une valeur lue à partir d’un document existant doit être maintenue à la précision d’origine complète ou être convertie en valeur UME.

Si l’implémentation ne parvient pas à effectuer cette opération, il doit avertir l’utilisateur que des données peuvent être perdues. (Il est possible d’émettre un tel avertissement une fois lorsque des données générées en externe sont rencontrées pour la première fois.)

Dans la pratique, les longueurs physiques sont utilisées pour des mesures relativement peu nombreuses dans cette proposition. Les données les plus importantes sont généralement les données de chemin d’accès et sont encodées dans le système de coordonnées défini, en fonction de la forme, par repère.

### <a name="alternative-representations"></a>Autres représentations

Les représentations de longueur standard du code HTML sont définies par [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) . Les unités relatives, à l’exception du pixel, ne sont pas significatives dans le contexte dans lequel les longueurs sont utilisées dans cette proposition et ne doivent pas être utilisées. Si le document enregistre la taille de pixel prévue (cible), cela définit la translation des pixels en EMU ; dans le cas contraire, la valeur par défaut de 90 dpi définie par [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) doit être utilisée.

À l’exception de l’UEM, toute valeur peut être fournie sous la forme d’une fraction décimale. Quand une valeur décimale est convertie en EMU, l’implémentation peut utiliser n’importe quel mode d’arrondi arithmétique. (Le seul moyen pour une application de création de garantir un résultat particulier est de la spécifier en UME.)

Si aucun spécificateur d’unité n’est fourni dans une valeur de longueur, l’implémentation doit supposer l’UEM.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="measure"></a>mesure


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



Une mesure est une quantité qui peut être une [longueur](#length) ou une [fraction](#fraction). Cela ressemble de près aux mesures de longueur HTML et CSS, qui peuvent, dans de nombreux cas, être des mesures physiques ou des pourcentages d’une autre quantité. Si aucun spécificateur d’unité n’est spécifié, la valeur doit être considérée comme une fraction décimale (ce comportement est donc hérité de la fraction, pas de la longueur).

Contrairement à la longueur, une valeur de pixel a une signification définie par le contexte, donc la conversion en EMU est normalement inappropriée. Il existe trois représentations fondamentales possibles que l’implémentation doit gérer (c’est-à-dire qu’une représentation ne peut pas être convertie en une autre sans perte d’informations).

1.  Une valeur fractionnaire doit être conservée au format [fraction](#fraction) (valeur « f »).
2.  Une longueur physique doit être maintenue en EMU.
3.  Une valeur de pixel doit être conservée en tant que nombre entier de pixels.

Les nombres fractionnaires de pixels ne sont pas autorisés.

### <a name="alternative-representations"></a>Autres représentations

Toutes les autres représentations de [fraction](#fraction) et de [longueur](#length) sont autorisées.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="angle"></a>angle


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



La représentation fondamentale d’un angle est un nombre de degrés multiple de 2 6 (65536) et stocké sous la forme d’un entier. Étant donné que l’espace de coordonnées est inversé (l’axe des y positif est inactif), un angle horaire est positif. Une implémentation conforme est requise pour conserver la précision totale d’une telle valeur.

Une implémentation est autorisée à utiliser n’importe quelle plage pour les angles et est autorisée à normalise un angle (par exemple, de-180 à + 180 ou de 0 à 360). Les implémentations ne doivent pas nécessairement être cohérentes ; Toutefois, la représentation intégrale d’un angle ne doit pas dépasser la plage d’un entier signé 32 bits.

Le suffixe FD est utilisé pour identifier cette représentation d’un angle (degré fractionnaire). Notez que cela est distingué du suffixe f pour une fraction sans dimension, même si une opération arithmétique identique peut être utilisée pour la prendre en charge. La valeur par défaut d’une valeur angulaire est un simple degré, c’est-à-dire une valeur non mise à l’échelle. Cela peut également être signalé par le suffixe «» (le symbole de degré). Toutefois, l’utilisation de cela dépend de la présence d’un encodage de document approprié. par conséquent, le suffixe deg est également défini pour signifier des degrés. L’ensemble des suffisants possibles est le suivant.



| Suffixe       | Facteur de conversion | Commentaires                               |
|--------------|-------------------|----------------------------------------|
| FD           | 1                 | Représentation interne haute précision |
| aucun, DEG,   | 65536             | Degrés                                |
| rad          | 65536pi/180       | Radians                                |



 

### <a name="alternative-representations"></a>Autres représentations

La transformation de mise à l’échelle présente des discontinuités à des multiples paires de 45. C’est pourquoi il est très important que la conversion de toute quantité inexacte soit bien définie. Pour cette raison, l’arithmétique de la conversion est définie pour arrondir à moins l’infini.

Étant donné que cela peut être difficile ou impossible à garantir dans certaines implémentations, l’utilisation des éléments suivants est définie comme une fonctionnalité de niveau 3 :

1.  Toute valeur de degré fractionnaire.
2.  Toute valeur en radian

Par conséquent, les valeurs des valeurs entières FD et Unqualified, ou des valeurs intégrales qualifiées deg ou doivent être gérées exactement par une implémentation de niveau 0 conforme ; Il n’est pas nécessaire d’utiliser d’autres valeurs. Il est fortement recommandé que toute implémentation traite la conversion d’une valeur de degré fractionnaire en valeur de degré mis à l’échelle (FD) exactement. Cela peut être effectué sans prise en charge de la virgule flottante.

Les exigences plus précises pour la conversion distinguent FD de f.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="color"></a>color


```HTML
c
<!element c  %color;>
```



Les couleurs constituent une partie essentielle des graphiques modernes des ordinateurs. La proposition utilise les méthodes établies pour spécifier des couleurs fixes. Toutefois, les couleurs des diagrammes sont rarement des couleurs statiques simples ; elles sont souvent dérivées d’autres éléments du diagramme. La plupart de ces informations sont propres à l’application. cette proposition fournit donc deux mécanismes très basiques pour spécifier un tel comportement :

1.  Une couleur peut être dérivée d’une autre couleur dans la même forme.
2.  Un petit nombre d’opérations arithmétiques sont définies pour la dérivation ou la modification d’une couleur.

Le mécanisme de forme prototype complète cela en autorisant la définition de prototypes à partir desquels les couleurs peuvent être héritées.


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



Une valeur de couleur est un sur-ensemble de la [définition de couleur CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) . Les extensions permettent de déterminer la valeur de couleur RVB à partir d’autres couleurs dans la forme ou à partir d’un modèle de couleurs global défini à l’aide de CSS1.

Si la valeur d’un élément est définie comme une couleur, le *contenu* d’un élément définit la valeur de couleur au moyen d’un jeton de couleur unique éventuellement modifié par une opération arithmétique sur la couleur RVB correspondante.

[![retour au début ](images/top.gif) en haut](#top)

### <a name="color-units"></a>Unités de couleur

L’ensemble complet des jetons de couleur provient de diverses sources : HTML, CSS1 et cette proposition. Ils sont définis comme suit à l’aide de la notation de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) ou de la notation XPointer définie pour la liaison XML.

Dans les définitions XPointer, la source d’emplacement est l’élément contenant la valeur de couleur, et l’expression fait référence au jeu d’éléments entier de la forme comme si des éléments de prototype de base avaient été fusionnés avec la forme. Lorsque l’élément correspondant n’existe pas, la valeur par défaut de cet élément est utilisée à la place.



| Couleur            | Définition                                                                                                  | Niveau | Description                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name             | Voir ci-dessous                                                                                                   | 0     | Nom de la couleur HTML, comme indiqué dans le tableau ci-dessous.                                                                                                                            |
| \#rr'gg'bb'      | \#rr'gg'bb'                                                                                                 | 0     | Représentation de couleur standard CSS1/sRVB utilisant des valeurs de la plage 0.. 255 représentées à l’aide de 2 chiffres hexadécimaux chacun.                                                     |
| \#composantes            | \#RRGGBB                                                                                                    | 1     | Formulaire CSS1 abrégé avec seulement trois chiffres hexadécimaux.                                                                                                                   |
| RGB (r, g, b)       | \#r activée p                                                                                                 | 1     | Forme CSS1 RGB ; les éléments de la valeur RVB sont convertis comme défini dans [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .                                      |
| fill             | ancêtre (1, forme)<br/> enfant (1, remplissage)<br/> enfant (1, couleur)<br/>                           | 1     | Couleur de remplissage de premier plan de la forme.                                                                                                                                   |
| fillBack         | ancêtre (1, forme)<br/> enfant (1, remplissage)<br/> enfant (1, précédent)<br/> enfant (1, couleur)<br/> | 1     | Couleur d’arrière-plan du remplissage de la forme.                                                                                                                                   |
| line             | ancêtre (1, forme)<br/> enfant (1, ligne)<br/> enfant (1, couleur)<br/>                           | 1     | Couleur de la ligne de premier plan de la forme.                                                                                                                                   |
| lineBack         | ancêtre (1, forme)<br/> enfant (1, ligne)<br/> enfant (1, précédent) <br/> enfant (1, couleur)<br/> | 1     | Couleur de ligne d’arrière-plan de la forme.                                                                                                                                   |
| lineOrFill       | trait, remplissage                                                                                                  | 1     | Valeur de ligne si elle n’est pas définie par défaut ; sinon, la valeur de remplissage. Cela retourne effectivement la couleur qui se trouve à l’extrémité de la forme.                                           |
| fillThenLine     | remplissage, ligne                                                                                                  | 1     | Valeur de remplissage si elle n’est pas définie par défaut ; sinon, la valeur de ligne. Cela renvoie effectivement la couleur principale de la forme (si la forme n’est pas remplie, le résultat est la couleur de ligne).   |
| shadow           | ancêtre (1, forme)<br/> enfant (1, ombre)<br/> enfant (1, couleur)<br/>                         | 2     | Couleur de l’ombre (il s’agit d’une fonctionnalité de niveau 2).                                                                                                                      |
| scheme           | Voir ci-dessous                                                                                                   | 1     | Couleur de schéma du schéma défini pour le document ; Voir ci-dessous.                                                                                                       |
| Scheme (*index*)  | Voir ci-dessous                                                                                                   | 1     | *Index* de couleurs du modèle, à partir de 0 ; Voir ci-dessous.                                                                                                                         |
| this             | Découle                                                                                                     | 2     | L’opération (remplissage d’un tracé ou dessin) est définie d’une autre façon (par exemple, en tant que bitmap), et la couleur spécifie une « modification » des couleurs, de cette façon. |
| palette (*index*) | Découle                                                                                                     | 3     | Se comporte de la même façon que cela, sauf qu’une seule entrée dans une table de couleurs de bitmap est identifiée. Autorisé uniquement lorsque l’énoncé explicite est spécifié.                             |
| aucun             | \-                                                                                                          | 2     | Indique l’absence d’une couleur ; peut être utilisé pour annuler une opération de dessin qui utilise la couleur.                                                                          |
| système           | Voir ci-dessous                                                                                                   | 3     | Couleur définie par l’interface utilisateur système.                                                                                                                             |



 

La couleur This permet à une valeur de couleur de spécifier une modification d’une couleur qui est dérivée d’une autre façon. en particulier, une seule opération peut être spécifiée pour toutes les couleurs d’une image bitmap. La couleur palette (*index*) identifie une entrée particulière dans une image bitmap mappée à la palette. L’utilisation de cet élément est uniquement définie pour l’enregistrement d’une entrée de table de couleurs qui doit être considérée comme transparente dans une telle image bitmap.

La définition d’une valeur de couleur ne doit pas faire référence à elle-même, directement ou indirectement. Si une telle définition est rencontrée, il est recommandé, mais pas obligatoire, que l’implémentation traite la valeur indéfinie comme étant noire.

[![retour au début ](images/top.gif) en haut](#top)

### <a name="html-colors"></a>Couleurs HTML

Le [code html](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) définit les seize noms de couleurs suivants :



Noms de couleurs et valeurs sRVB

![Exemple de couleur noire.](images/black.gif)

Black = " \# 000000"

![Exemple de couleur verte.](images/green.gif)

Vert = « \# 008000 »

![Exemple de couleur Silver.](images/silver.gif)

Silver = « \# C0C0C0 »

![Exemple de couleur citron.](images/lime.gif)

Citron = " \# 00FF00"

![Exemple de couleur grise.](images/gray.gif)

Gray = " \# 808080"

![Exemple de couleur d’olive.](images/olive.gif)

Olive = " \# 808000"

![Exemple de couleur blanche.](images/white.gif)

Blanc = " \# FFFFFF"

![Exemple de couleur ywllow.](images/yellow.gif)

Yellow = " \# FFFF00"

![Exemple de couleur marron.](images/maroon.gif)

Marron = " \# 800000"

![Exemple de couleur marine.](images/navy.gif)

Bleu foncé = " \# 000080"

![Exemple de couleur rouge.](images/red.gif)

Rouge = « \# FF0000 »

![Exemple de couleur bleue.](images/blue.gif)

Blue = « \# 0000FF »

![Exemple de couleur violette.](images/purple.gif)

Violet = " \# 800080"

![Exemple de couleur bleu-vert.](images/teal.gif)

Bleu-vert = « \# 008080 »

![Exemple de couleur fuchsia.](images/fuchsia.gif)

Fuchsia = " \# FF00FF"

![Exemple de couleur cyan.](images/aqua.gif)

Cyan = « \# 00FFFF »



 

[![retour au début ](images/top.gif) en haut](#top)

### <a name="scheme-colors"></a>Couleurs du schéma

Les couleurs de schéma référencées par le modèle sont définies au niveau du document à l’aide de la balise méta avec l’attribut de nom « jeu de couleurs de thème ».


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



Cette balise permet de définir jusqu’à huit couleurs de schéma. Les couleurs non définies doivent par défaut être noires. Les couleurs du schéma permettent de modifier le jeu de couleurs utilisé pour un document complet simplement en modifiant le contenu du jeu de couleurs du thème. Pour vous assurer que les graphiques importés à partir de différentes applications de création utilisent de manière cohérente les couleurs du schéma, les interprétations suivantes sont définies. « Utilisation » est une brève description de l’objectif et la colonne « Description » fournit des détails supplémentaires.



| Index | Nom              | Usage                         | Description                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 0     | Scheme. Background | Arrière-plan                    | Couleur utilisée pour l’arrière-plan d’un graphique (et, souvent, pour la page entière).                                    |
| 1     | Scheme. Text       | Texte et lignes                | Couleur du texte attaché à une forme et la couleur de ligne standard.                                                      |
| 2     | schéma. Shadow     | Ombres                       | Couleur de l’ombre standard : couleur généralement utilisée pour les ombres des formes.                                                     |
| 3     | Scheme. title      | Texte du titre                    | Couleur à utiliser pour le titre ou le texte du titre.                                                                              |
| 4     | Scheme. Fill       | Remplit                         | Couleur de remplissage standard : couleur généralement utilisée pour remplir les formes.                                                          |
| 5     | Scheme. accent     | Non                        | Couleur de mise en surbrillance normale utilisée pour mettre en relief un élément important d’un graphique.                                             |
| 6     | Scheme. HYPERLINK  | Accent et lien hypertexte          | Couleur de surbrillance utilisée pour les liens hypertexte. Peut être utilisé à d’autres fins lorsque la couleur désigne un lien vers d’autres informations. |
| 7     | schéma. suivi   | Accent et lien hypertexte visité | Couleur de surbrillance pour les liens hypertexte visités ; également adapté aux liens « en arrière ».                                         |



 

Une couleur de schéma peut être référencée par son nom ou par son index, de sorte que Scheme. Fill et Scheme (4) sont de la même couleur.

Les couleurs de schéma ne participent pas au schéma par défaut si aucune couleur n’est spécifiée. Une couleur de remplissage non spécifiée doit toujours être interprétée en tant que blanc, quelle que soit la couleur du jeu de couleurs 4. Les couleurs « accent » doivent être contrastées avec les couleurs d’arrière-plan (0) et de remplissage (4), tandis que les couleurs de texte et de texte du titre doivent avoir la même propriété. Une technique standard consiste à rendre les accents colorés et le texte standard non coloré (généralement en noir ou blanc).

[![retour au début ](images/top.gif) en haut](#top)

### <a name="system-colors"></a>Couleurs système

Les applications enregistrent parfois des couleurs en fonction des paramètres du système d’exploitation dans les graphiques. Normalement, ceux-ci sont temporaires et n’ont pas besoin d’être écrits ; les définitions thesystemcolor existent uniquement pour prendre en charge cette fonctionnalité. Une couleur système est introduite en définissant une balise appropriée dans un nouvel espace de noms et en insérant les informations appropriées dans le contenu de l’élément.

cette proposition définit une telle balise pour encoder les Windows couleurs de l’interface utilisateur définies dans le fichier d’en-tête winuser. h.


```HTML
win.color
<!element win.color #pcdata>
```



Le contenu de l’élément est un entier unique qui contient la valeur de la définition de couleur appropriée \_ de winuser. h. Une technique similaire peut être adoptée pour toute spécification de couleur propre au système ou à l’application. Il est fortement recommandé d’utiliser cette fonctionnalité uniquement pour la compatibilité descendante.

[![retour au début ](images/top.gif) en haut](#top)

### <a name="pure-colors"></a>Couleurs pures


```HTML
pure
<!elementpure empty>
```



Si l’élément <pure/> apparaît dans une valeur de couleur, il s’agit d’une indication que la couleur ne doit pas être approximative par un modèle de trame. Il s’agit d’une fonctionnalité de niveau 1, et une implémentation conforme n’a pas besoin d’être respectée. La désignation est importante pour les graphiques affichés sur des appareils de résolution moyenne, tels que les affichages vidéo, où les petites fonctionnalités (telles que les lignes) peuvent provoquer des alias erronés avec des couleurs dépendantes. Sur les appareils tels que les imprimantes, qui déforment normalement toutes les couleurs, à l’exception des quelques couleurs entièrement saturées, le tramage est normalement suffisamment suffisant pour éviter ce problème.

[![retour au début ](images/top.gif) en haut](#top)

### <a name="color-adjustments"></a>Réglages des couleurs

La couleur de base peut être ajustée par des opérations arithmétiques sur la valeur RVB. Ces opérations sont définies à l’aide d’éléments supplémentaires dans la valeur de couleur. De tels ajustements sont utiles uniquement lorsqu’ils sont appliqués à des couleurs dérivées d’autres éléments. Il est possible de spécifier un tel ajustement sur une valeur de couleur fixe ; Toutefois, une implémentation est autorisée à réduire cela à la valeur RVB correspondante et à la stocker à la place de l’original.

Toutes les fonctionnalités de réglage des couleurs décrites dans cette section sont des fonctionnalités de niveau 1.


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



Le paramètre des six premières opérations est une valeur numérique intégrale unique comprise entre 0 et 255. L’ajustement est effectué sur la valeur RGB 3x8bit comme suit :

1.  Si <gray/> est spécifié, la valeur RVB est remplacée par YYY, où y est la valeur de luminance (y) calculée à partir de la valeur sRVB en suivant l’ITU-r BT. 709. Ce calcul est le suivant :
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  Si une modification Color. op est donnée, chaque composant est ajusté séparément en fonction du tableau ci-dessous. c est la valeur du composant, et p est la valeur Color. Parameter.

    | Opération       | Formule                            |
    |-----------------|------------------------------------|
    | fonce          | c : = CXP/255                       |
    | Light         | c : = 255-(255-c) XP/255           |
    | ajouter             | c : = c + p                         |
    | soustraction        | c : = c-p                         |
    | reversesubtract | c : = p-c                         |
    | blackwhite      | Si c < p thenc : = 0elsec : = 255 |

    

     

    Dans chaque cas, si la valeur du composant calculé, c, est supérieure à 255, 255 est utilisé et, s’il est inférieur à 0, la valeur 0 est utilisée.

3.  Si <INVERT128/> est donné, la valeur 128 est soustraite ou ajoutée à chaque composant selon que le composant est inférieur à 128 ou non.
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  Si <invert/> est donné, chaque composant est remplacé par 255 moins la valeur du composant.
    ```HTML
    c := 255-c
    ```

    

[![retour au début ](images/top.gif) en haut](#top)

## <a name="font"></a>son


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



Une police est identifiée à l’aide d’un attribut de style tel que défini dans la [section CSS1 5,2 (propriétés de police)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) . Le corps de l’élément de police est, à l’heure actuelle, non défini, mais peut être utilisé à l’avenir pour encoder les informations de police standard. Les implémentations initiales de cette proposition doivent conserver les informations, mais pas les interpréter.

Il est concevable que la prise en charge soit ajoutée à l’avenir pour les informations de police hors ligne (polices téléchargeables ou ressources de police partagées). Cette opération est effectuée par un élément de lien XML dans le contenu de l’élément font, garantissant la compatbility descendante avec les implémentations initiales.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="bitmap"></a>bitmap


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



L’élément bitmap autorise une référence à une ressource d’image hors ligne (normalement une image bitmap) à inclure dans un graphique.

la bitmap est une fonctionnalité de niveau 1.

L’attribut Behavior peut être utilisé pour indiquer comment la bitmap doit être gérée par une application de modification. La valeur peut être l’un des jetons suivants (ou les deux).



| par jeton    | Description                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| séparé | Marque l’image bitmap comme une entité distincte, qui ne doit pas être considérée comme une partie intégrante du document. L’image bitmap ne doit pas être conservée avec le document. Si le document est copié, l’image bitmap ne doit pas être copiée ; Si le document est déplacé, l’image bitmap ne doit pas être déplacée. |
| ressource d’origine | L’attribut title identifie l’emplacement d’origine de l’image bitmap comme une URL ; dans le cas contraire, la signification du titre n’est pas spécifiée.                                                                                                                                                          |



 

Ces valeurs sont à la fois des indications sur le comportement attendu. L’option distinct fait référence au comportement des données référencées par href. Si les deux éléments sont distincts et originaux, l’application est censée ignorer l’URI href et régénérer l’image bitmap à partir des données d’origine. Si seul l’original est donné, l’application est censée utiliser l’URI href pour trouver la bitmap, mais peut donner à l’utilisateur la possibilité de la régénérer.

Il est possible de donner à l’URI href et à l’attribut title la même valeur (lexicale), ce qui est approprié si le bitmap référencé n’est pas « stocké avec » dans le document. Il est prévu (même s’il n’est pas obligatoire) que href soit utilisé pour la copie de l’image bitmap du document, qui peut être supprimé si les formes de référence sont supprimées, et que ce titre doit être utilisé pour indiquer une copie partagée. Par conséquent, si les deux contiennent la même valeur, il n’y a pas de copie spécifique au document.

Les applications peuvent ignorer l’indication si elles ne tiennent pas dans le modèle de stockage réel des données XML.

[![retour au début ](images/top.gif) en haut](#top)

### <a name="picture-file-formats"></a>Formats de fichiers image

Dans le contexte de cette proposition, les données externes sont invariablement une image bitmap ou un fichier qui est utilisé pour produire une image bitmap. Au niveau de rendu 0, aucun format de bitmap externe ne doit être pris en charge--les chemins d’accès peuvent uniquement être remplis avec des couleurs unies. Pour afficher l’ensemble complet des remplissages de niveau 1, les bitmaps doivent être prises en charge. Le niveau de rendu 1 comprend (uniquement) les formats suivants :

1.  JFIF, c’est-à-dire les données de format ISO/IEC 10918 incorporées dans un fichier avec l’en-tête JFIF (qui peut être considéré comme un marqueur APP0 particulier après le fabricant SOI-ci) et incluant (uniquement) la plage de formats JPEG prise en charge par le code IJG V6.
2.  PNG, tel que défini par la spécification PNG version 1,0.

Le niveau de rendu 2 prend également en charge les éléments suivants :

-   GIF, tel que défini par la spécification GIF publiée par CompuServ dans 1987 (généralement appelé « GIF87a »). GIF89a doit également être pris en charge à ce niveau, en fonction de la restriction selon laquelle les données ne doivent pas contenir de blocs d’extension nécessitant une interprétation pour afficher la bitmap autre que Graphics Control extensionswithouta requirement pour l’entrée utilisateur ou un délai. Cela permet d’inclure des commentaires, mais pas l’extension de texte brut. Une application peut insérer des extensions d’application (0x21, 0xFF) mais, à l’aide de la terminologie de cette proposition, celles-ci ne doivent contenir que des données de modification, et non de rendu.

Tout autre format de données utilisé dans le graphique force ce graphique à avoir au moins un niveau de modification 3 et éventuellement un niveau de rendu 3 (si les données sont nécessaires pour effectuer le rendu du graphique). Une application est encouragée à publier les formats qu’elle prend en charge. par exemple, Microsoft Office prend en charge les formats supplémentaires suivants en mode natif et peut donc écrire des données de modification dans ce formulaire :

1.  WMF--Windows metafile (format Win 3,1)
2.  EMF--Windows métafichier « amélioré » (format Win32)
3.  PICT--Mac OS fichier. QuickDraw PICT (toutes les versions, mais sans enregistrements QuickTime ou autres extensions)
4.  BMP--Windows format de fichier bitmap, « os/2 » (BITMAPCORE), bitmapinfo,, BITMAPV4 et BITMAPV5 formats

[![retour au début ](images/top.gif) en haut](#top)

## <a name="vector"></a>vecteur


```HTML
v
<!element v "( #pcdata | p )*">
```



Un tracé graphique vectoriel est encodé en tant que PCDATA. Le contenu de l’élément v est mélangé, contenant une description du chemin d’accès du vecteur éventuellement paramétrable avec des éléments p.

[Retour à la vue d’ensemble du VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

