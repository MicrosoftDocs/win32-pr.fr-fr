---
description: Le format de texture DXT1 est pour les textures opaques ou qui ont une seule couleur transparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Textures opaques et alpha 1 bits (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104562069"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a>Textures opaques et alpha 1 bits (Direct3D 9)

Le format de texture DXT1 est pour les textures opaques ou qui ont une seule couleur transparente.

Pour chaque bloc alpha opaque ou 1 bit, les valeurs 2 16 bits (format RVB 5:6:5) et une image bitmap 4x4 avec 2 bits par pixel sont stockées. Cela totalise 64 bits pour 16 texels, ou quatre bits par Texel. Dans la bitmap de bloc, il y a 2 bits par Texel pour choisir entre les quatre couleurs, deux d’entre elles étant stockées dans les données encodées. Les deux autres couleurs sont dérivées de ces couleurs stockées par interpolation linéaire. Cette disposition est présentée dans le diagramme suivant.

![diagramme de la disposition bitmap](images/colors1.png)

Le format alpha de 1 bit est distingué du format opaque en comparant les valeurs de couleur 2 16 bits stockées dans le bloc. Ils sont traités comme des entiers non signés. Si la première couleur est supérieure à la seconde, cela implique que seules les éléments de texture opaques sont définis. Cela signifie que quatre couleurs sont utilisées pour représenter les texels. Dans un encodage en quatre couleurs, il existe deux couleurs dérivées et les quatre couleurs sont également réparties dans l’espace de couleurs RVB. Ce format est similaire au format RVB 5:6:5. Sinon, pour la transparence alpha de 1 bit, trois couleurs sont utilisées et le quatrième est réservé pour représenter des texels transparents.

Dans un encodage en trois couleurs, il existe une couleur dérivée et le quatrième code 2 bits est réservé pour indiquer une Texel transparente (informations alpha). Ce format est analogue à RVBA 5:5:5:1, où le bit final est utilisé pour l’encodage du masque Alpha.

L’exemple de code suivant illustre l’algorithme permettant de déterminer si l’encodage à trois ou quatre couleurs est sélectionné :


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



Il est recommandé de définir les composants RVBA du pixel de transparence sur zéro avant la fusion.

Les tableaux suivants indiquent la disposition de la mémoire pour le bloc de 8 octets. Il est supposé que le premier index correspond à la coordonnée y et le second correspond à la coordonnée x. Par exemple, Texel \[ 1 \] \[ 2 \] fait référence au pixel de la carte de texture à (x, y) = (2, 1).

Ce tableau contient la disposition de la mémoire pour le bloc de 8 octets (64 bits).



| Adresse du mot | mot 16 bits    |
|--------------|----------------|
| 0            | Couleur \_ 0       |
| 1            | Couleur \_ 1       |
| 2            | Mot bitmap \_ 0 |
| 3            | Mot bitmap \_ 1 |



 

\_La couleur 0 et \_ la couleur 1, les couleurs aux deux extrêmes sont présentées comme suit :



| Bits        | Couleur                 |
|-------------|-----------------------|
| 4:0 (LSB \* ) | Composant de couleur bleu  |
| 10:5        | Composant de couleur verte |
| 15:11       | Composant de couleur rouge   |



 

\*bit le moins significatif

Le mot bitmap \_ 0 est disposé comme suit :



| Bits          | Texel           |
|---------------|-----------------|
| 1:0 (LSB)     | Texel \[ 0 \] \[ 0\] |
| 3:2           | Texel \[ 0 \] \[ 1\] |
| 5:4           | Texel \[ 0 \] \[ 2\] |
| 7:6           | Texel \[ 0 \] \[ 3\] |
| 9:8           | Texel \[ 1 \] \[ 0\] |
| 11:10         | Texel \[ 1 \] \[ 1\] |
| 13:12         | Texel \[ 1 \] \[ 2\] |
| 15:14 (MSB \* ) | Texel \[ 1 \] \[ 3\] |



 

\*bit le plus significatif (MSB)

Le mot bitmap \_ 1 est disposé comme suit :



| Bits        | Texel           |
|-------------|-----------------|
| 1:0 (LSB)   | Texel \[ 2 \] \[ 0\] |
| 3:2         | Texel \[ 2 \] \[ 1\] |
| 5:4         | Texel \[ 2 \] \[ 2\] |
| 7:6         | Texel \[ 2 \] \[ 3\] |
| 9:8         | Texel \[ 3 \] \[ 0\] |
| 11:10       | Texel \[ 3 \] \[ 1\] |
| 13:12       | Texel \[ 3 \] \[ 2\] |
| 15:14 (MSB) | Texel \[ 3 \] \[ 3\] |



 

## <a name="example-of-opaque-color-encoding"></a>Exemple d’encodage de couleur opaque

En guise d’exemple d’encodage opaque, supposons que les couleurs rouge et noir sont à l’extrême. Le rouge est la couleur \_ 0 et le noir est la couleur \_ 1. Quatre couleurs interpolées forment le dégradé uniformément réparti entre eux. Pour déterminer les valeurs de la bitmap 4x4, les calculs suivants sont utilisés :


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



Le bitmap ressemble alors au diagramme suivant.

![Diagramme qui affiche la disposition bitmap développée.](images/colors2.png)

Cela ressemble à la série de couleurs illustrée ci-dessous.

> [!Note]  
> Dans une image, pixel (0,0) apparaît en haut à gauche.

 

![illustration d’un dégradé encodé opaque](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a>Exemple d’encodage alpha 1 bits

Ce format est sélectionné lorsque l’entier non signé 16 bits, Color \_ 0, est inférieur à l’entier 16 bits non signé, Color \_ 1. Un exemple de ce format peut être utilisé dans une arborescence, par rapport à un ciel bleu. Certains texels peuvent être marqués comme étant transparents alors que trois nuances de vert sont toujours disponibles pour les feuilles. Deux couleurs corrigent les extrêmes, tandis que la troisième est une couleur interpolée.

L’illustration suivante est un exemple d’une telle image.

![illustration de l’encodage alpha 1 bits](images/greenthing.png)

Notez que lorsque l’image est affichée en blanc, le Texel est encodé comme transparent. Notez également que les composants RVBA des texels transparents doivent être définis sur zéro avant la fusion.

L’encodage bitmap des couleurs et de la transparence est déterminé à l’aide des calculs suivants.


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



Le bitmap ressemble alors au diagramme suivant.

![diagramme de la disposition bitmap développée](images/colors3.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources de texture compressées](compressed-texture-resources.md)
</dt> </dl>

 

 



