---
description: Les applications qui utilisent les métriques de texte TrueType peuvent obtenir un haut niveau de portabilité des imprimantes et des documents ; ils peuvent utiliser des métriques TrueType même s’ils doivent assurer la compatibilité avec les premières versions 16 bits de Windows.
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: Utilisation des métriques TrueType portables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb56eaa3111dad8592b1e1f6edbab2a64ced6e2a6c9b6e1a94baf8a5acc7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848999"
---
# <a name="using-portable-truetype-metrics"></a>Utilisation des métriques TrueType portables

Les applications qui utilisent les métriques de texte TrueType peuvent obtenir un haut niveau de portabilité des imprimantes et des documents ; ils peuvent utiliser des métriques TrueType même s’ils doivent assurer la compatibilité avec les premières versions 16 bits de Windows.

Les largeurs de conception contourneront la plupart des problèmes de texte dépendant des appareils introduits par des appareils physiques. Les largeurs de conception sont un type de largeur logique. Indépendamment des problèmes de pixellisation ou de la mise à l’échelle des transformations, chaque glyphe a une largeur et une hauteur logique. Composé d’une page logique, chaque caractère d’une chaîne a un emplacement qui est indépendant des largeurs de l’appareil physique. Bien qu’une largeur logique implique que les largeurs puissent être mises à l’échelle de façon linéaire à toutes les tailles de points, cela n’est pas nécessairement vrai pour les polices non portables ou les polices TrueType. À des tailles plus petites, certains glyphes sont rendus plus larges par rapport à leur hauteur pour une meilleure lisibilité.

Les caractères des polices principales TrueType sont conçus par rapport à une grille 2048 par 2048. La largeur de la conception est la largeur d’un caractère dans ces unités de grille. (TrueType prend en charge toute taille de grille entière allant jusqu’à 16 384 par 16 384 ; les tailles de grille qui sont des valeurs entières de 2 évoluent plus rapidement que les autres tailles de grille.)

Le contour de la police est conçu en unités fictives. Le carré em est la grille notionnelle par rapport à laquelle le contour de la police est ajusté. (Vous pouvez utiliser le membre **otmEMSquare** de [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) et le membre **ntmSizeEM** de [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) pour récupérer la taille du carré em en unités fictives.) Lors de la création d’une police dont la taille en points (en unités de périphérique) est égale à la taille de son carré em, les largeurs ABC pour cette police sont les largeurs de conception souhaitées. Par exemple, supposons que la taille d’un carré cadratin soit 1000 et que la largeur ABC d’un caractère de la police soit 150, 400 et 150. Dans cette police, un caractère de 10 unités de périphérique a une largeur ABC de 1,5, 4 et 1,5, respectivement. Étant donné que le \_ mode de mappage de texte mm est le plus souvent utilisé avec les polices (et que le \_ texte de mm est équivalent aux unités de périphérique), il s’agit d’un calcul simple.

En raison de la haute résolution des largeurs de conception TrueType, les applications qui les utilisent doivent prendre en compte les valeurs numériques volumineuses qui peuvent être créées. Pour plus d'informations, voir les rubriques suivantes :

-   [Unité et unités de conception](device-vs--design-units.md)
-   [Mesures pour les documents portables](metrics-for-portable-documents.md)

 

 



