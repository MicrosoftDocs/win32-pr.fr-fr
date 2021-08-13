---
description: Quand une application appelle une fonction de dessin pour peindre une forme, le système positionne un pinceau au début de l’opération de peinture et mappe un pixel dans le pinceau bitmap à la zone cliente à l’origine de la fenêtre, qui est l’angle supérieur gauche de la fenêtre.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origine du pinceau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ccdc1dfa370ceb84216c89d562ef56dd206ce744b3be4fd38deb87175c1cf73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400389"
---
# <a name="brush-origin"></a>Origine du pinceau

Quand une application appelle une fonction de dessin pour peindre une forme, le système positionne un pinceau au début de l’opération de peinture et mappe un pixel dans le pinceau bitmap à la zone cliente à l’origine de la *fenêtre*, qui est l’angle supérieur gauche de la fenêtre. Les coordonnées du pixel que les mappages système sont appelées l' *origine du pinceau*. L’origine du pinceau par défaut se trouve dans le coin supérieur gauche de l’image bitmap du pinceau, aux coordonnées (0,0). Le système copie ensuite le pinceau dans la zone cliente, en formant un modèle aussi grand que l’image bitmap. L’opération de copie continue, ligne par ligne, jusqu’à ce que la totalité de la zone cliente soit remplie. Toutefois, le motif de pinceau est visible uniquement dans les limites de la forme spécifiée.

Il y a des instances lorsque l’origine du pinceau par défaut ne doit pas être utilisée. Par exemple, il peut être nécessaire pour une application d’utiliser le même pinceau pour peindre les arrière-plans de ses fenêtres parent et enfant et de fusionner l’arrière-plan d’une fenêtre enfant avec celle de la fenêtre parente. Pour ce faire, l’application doit réinitialiser l’origine du pinceau en appelant la fonction [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) et en décalant le nombre requis de pixels de l’origine. (Une application peut récupérer l’origine du pinceau en cours en appelant la fonction [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .)

L’illustration suivante montre une étoile à cinq branches remplie à l’aide d’un pinceau défini par l’application. L’illustration montre une image avec zoom du pinceau, ainsi que l’emplacement auquel elle a été mappée au début de l’opération de peinture.

![Illustration montrant que l’origine du pinceau est mappée à l’origine de la fenêtre](images/csbru-01.png)

 

 



