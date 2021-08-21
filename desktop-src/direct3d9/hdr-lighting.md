---
description: L’éclairage dans le monde réel contient une plage dynamique très élevée (HDR) de valeurs de luminance.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Éclairage HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863e8eefab6e0199904876bdb398fefa1aeb988ef2f3556b21c24d92dbc998e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094645"
---
# <a name="hdr-lighting-direct3d-9"></a>Éclairage HDR (Direct3D 9)

L’éclairage dans le monde réel contient une plage dynamique très élevée (HDR) de valeurs de luminance. Le monde réel compte environ 10 commandes de plages dynamiques (DR) pour les valeurs de luminance réparties dans le spectre d’obscurité à la luminosité. En revanche, un écran d’ordinateur a une gamme d’affichage très limitée (ou une plage de valeurs de luminance) : environ deux commandes de plage dynamique. La difficulté à produire des images de rendu HDR consiste à mapper les valeurs HDR réelles dans la gamme limitée d’un écran d’ordinateur.

Le mappage de tonalité est la technique utilisée par DirectX pour mapper les informations HDR dans une plage plus limitée. Le mappage de tonalité appliqué au rendu CGI peut améliorer considérablement la quantité de détails d’éclairage rendue, ce qui permet d’afficher des détails dans les zones les plus sombres et de fournir un contraste dans les zones qui sont tellement brillantes. Les scènes résultantes sont rendues avec des détails d’éclairage bien plus visibles.

L' [exemple HDRLighting](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) est un kit de développement logiciel (SDK) qui illustre l’éclairage HDR.

## <a name="tone-mapping"></a>Correspondance des tons

Le placage de ton simule généralement des phénomènes optiques qui ne peuvent pas être provoqués par la récupération d’urgence du moniteur. Il s’agit, par exemple, de halos ou de la floraison (principalement des propriétés de lentilles), du décalage bleu qui se produit dans l’oeil humain en conditions d’éclairage faible et d’autres adaptations qui résultent de la biochimie de l’oeil. Si la récupération d’urgence de l’affichage était assez grande, le mappage de tonalité n’est pas si nécessaire, à l’exception de la fourniture d’effets artistiques ou de certaines propriétés d’une lentille d’appareil photo ou d’un appareil à couplage de frais (CCD).

Le placage de tons divise la plage de valeurs de luminance dans une scène en un ensemble de zones. Chaque zone englobe une plage de valeurs de luminance.

HDR utilise les termes suivants :

-   Plage de valeurs de luminance dans une zone
-   Gris moyen-zone de luminosité du milieu de la scène
-   Taux de plage dynamique de la luminance de scène la plus élevée à la luminance de scène la plus faible
-   Mesure d’éclairage de scène clé-subjective : elle varie d’un clair à l’obscurité

Pour calculer la luminance à partir des valeurs RVB, utilisez ce qui suit :


```
L = 0.27R + 0.67G + 0.06B;
```



La luminance moyenne des journaux est une approximation utile pour la clé d’une scène. Une équation générale se présente comme suit :

L<sub>w</sub> = exp \[ 1/N ( \[ Journal Sum (Delta + L<sub>w</sub>(x, y)) \] ) \]

Où :

-   L<sub>w</sub> -log-luminance moyenne
-   N-nombre de pixels dans l’image
-   Delta : petit facteur permettant d’éviter les problèmes avec les pixels noirs
-   L<sub>w</sub>(x, y)-la luminance de l’espace universel pour le pixel (x, y)

Pour le mapper à une valeur de gris moyen, voici un opérateur de mise à l’échelle de luminance :

L (x, y) = a \* l<sub>w</sub>(x, y)/l<sub>w</sub>

Où :

-   L (x, y)-luminance à l’échelle pour le pixel (x, y)
-   valeur de clé-image après l’application de la mise à l’échelle

Enfin, voici un opérateur de mappage de ton simple pour compresser les luminances élevées :

L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))

Où :

-   L<sub>(</sub>x, y)-luminance compressée et mise à l’échelle pour le pixel (x, y)
-   valeur de clé-image après l’application de la mise à l’échelle

Cet opérateur met à l’échelle les luminances élevées par 1/L et les luminances basses de 1. Pour plus d’informations, consultez le document suivant.

Reinhard, Erik, Mike, Peter Shirley et James Ferwerda. [« Reproduction des sons photographiques pour les images numériques »](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf). Transactions ACM sur Graphics (TOG), procédure du 29 Conférence annuelle sur les graphiques informatiques et les techniques interactives (SIGGRAPH), pp. 267-276. New York, NY : ACM Press, 2002.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> </dl>

 

 



