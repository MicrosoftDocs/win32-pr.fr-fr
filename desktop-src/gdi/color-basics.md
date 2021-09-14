---
description: Les fonctionnalités de couleur des appareils, telles que les affichages et les imprimantes, peuvent aller de monochrome à des milliers de couleurs.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Notions de base des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227897"
---
# <a name="color-basics"></a>Notions de base des couleurs

Les fonctionnalités de couleur des appareils, telles que les affichages et les imprimantes, peuvent aller de monochrome à des milliers de couleurs. Étant donné qu’une application peut avoir besoin de générer une sortie pour des appareils dans cette plage, elle doit être préparée à gérer des fonctionnalités de couleur variables.

Une application peut découvrir le nombre de couleurs disponibles pour un appareil donné à l’aide de la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) pour récupérer la valeur NUMCOLORS. Cette valeur spécifie le nombre de couleurs pouvant être utilisées par l’application. En règle générale, ce nombre correspond à une propriété physique du périphérique de sortie, par exemple le nombre d’encres de l’imprimante ou le nombre de signaux de couleur distincts que la carte vidéo peut transmettre à l’analyse.

Bien que la valeur NUMCOLORS spécifie le nombre de couleurs, elle n’identifie pas les couleurs disponibles. Une application peut découvrir les couleurs disponibles en énumérant tous les stylets ayant le \_ type solide PS. Étant donné que le pilote de périphérique qui prend en charge un appareil donné possède généralement une gamme complète de stylets pleins et que le système nécessite que les plumes solides aient uniquement des couleurs que l’appareil peut générer, l’énumération de ces stylets est souvent équivalente à l’énumération des couleurs. Une application peut énumérer les stylets à l’aide de la fonction [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) . Pour obtenir un exemple de code, consultez [énumération des couleurs](enumerating-colors.md).

Pour plus d'informations, voir les rubriques suivantes :

-   [Valeurs de couleur](color-values.md)
-   [Approximations de couleurs et tramage](color-approximations-and-dithering.md)
-   [Couleur dans les bitmaps](color-in-bitmaps.md)
-   [Mélange de couleurs](color-mixing.md)

 

 



