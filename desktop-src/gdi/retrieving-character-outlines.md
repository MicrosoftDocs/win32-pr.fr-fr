---
description: Vous pouvez utiliser la fonction GetGlyphOutline pour récupérer le contour d’un glyphe à partir d’une police TrueType.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Récupération des contours de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3db9b9200f665088096fdecbffc12866668d093c0c4d5ddb4a1612153873e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092649"
---
# <a name="retrieving-character-outlines"></a>Récupération des contours de caractères

Vous pouvez utiliser la fonction [GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) pour récupérer le contour d’un glyphe à partir d’une police TrueType. Le contour du glyphe retourné par la fonction [**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) est pour un glyphe ajusté à la grille. (Un glyphe ajusté à la grille a été modifié afin que son image bitmap soit aussi proche que possible de la conception d’origine du glyphe.) Si votre application nécessite un contour de glyphe non modifié, demandez la structure du glyphe pour un caractère dans une police dont la taille est égale aux unités em de la police. (Pour créer une police avec cette taille, définissez le membre **lfHeight** de la structure [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) sur la valeur négative de la valeur du membre **ntmSizeEM** de la structure [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .)

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) retourne le contour sous la forme d’une image bitmap ou d’une série de polylignes et de splines. Quand une application récupère un contour de glyphe sous la forme d’une série de polylignes et de splines, les informations sont retournées dans une structure [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) suivie de autant de structures [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) que nécessaire pour décrire le glyphe. Tous les points sont retournés en tant que structures [POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) et représentent des positions absolues, et non des déplacements relatifs. Le point de départ spécifié par le membre **pfxStart** de la structure [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) est le point où commence le contour d’un contour. Les structures [**TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) qui suivent peuvent être des enregistrements de type polyligne ou des enregistrements de spline.

Pour afficher un contour de caractère TrueType, vous devez utiliser à la fois les enregistrements Polyline et spline. Le système peut restituer des polylignes et des splines facilement. Chaque enregistrement polyligne et spline contient autant de points séquentiels que possible, afin de réduire le nombre d’enregistrements retournés.

Le point de départ spécifié dans la structure [**TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) est toujours sur le contour du glyphe. Le point spécifié sert à la fois de points de départ et de fin pour le contour.

Cette section fournit des informations sur les rubriques suivantes.

-   [Enregistrements Polyline](polyline-records.md)
-   [Enregistrements spline](spline-records.md)

 

 
