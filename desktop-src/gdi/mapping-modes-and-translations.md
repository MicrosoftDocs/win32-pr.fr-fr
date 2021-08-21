---
description: Les modes de mappage sont décrits dans le tableau suivant.
ms.assetid: 02bc45d1-2921-48bc-a066-2314765b6531
title: Modes de mappage et traductions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242ba699a8ec7289495cbcdff33e940460b20bcabffa373d5c792b1aee0fe9d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760145"
---
# <a name="mapping-modes-and-translations"></a>Modes de mappage et traductions

Les modes de mappage sont décrits dans le tableau suivant.



| Mode de mappage    | Description                                                                                                                                                                                                                                                                                                                |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MM \_ anisotrope | Chaque unité de l’espace de page est mappée à une unité spécifiée par l’application dans l’espace de l’appareil. L’axe peut être ou ne pas être mis à l’échelle de façon égale (par exemple, un cercle dessiné dans le monde peut apparaître comme une ellipse lorsqu’il est représenté sur un appareil donné). L’orientation de l’axe est également spécifiée par l’application.                  |
| \_HIENGLISH mm   | Chaque unité de l’espace de page est mappée à 0,001 de pouce dans l’espace de l’appareil. La valeur de x augmente de gauche à droite. La valeur de y augmente de bas en haut.                                                                                                                                                                 |
| \_HIMETRIC mm    | Chaque unité de l’espace de page est mappée à 0,01 millimètres dans l’espace de l’appareil. La valeur de x augmente de gauche à droite. La valeur de y augmente de bas en haut.                                                                                                                                                            |
| MM \_ isotrope   | Chaque unité de l’espace de page est mappée à une unité définie par l’application dans l’espace de l’appareil. Les axes sont toujours mis à l’échelle de manière égale. L’orientation des axes peut être spécifiée par l’application.                                                                                                                                     |
| \_LOENGLISH mm   | Chaque unité de l’espace de page est mappée à 0,01 de pouce dans l’espace de l’appareil. La valeur de x augmente de gauche à droite. La valeur de y augmente de bas en haut.                                                                                                                                                                  |
| \_LOMETRIC mm    | Chaque unité de l’espace de page est mappée à 0,1 millimètres dans l’espace de l’appareil. La valeur de x augmente de gauche à droite. La valeur de y augmente de bas en haut.                                                                                                                                                             |
| \_texte mm        | Chaque unité de l’espace de page est mappée à un pixel ; autrement dit, aucune mise à l’échelle n’est effectuée. Si aucune traduction n’est en vigueur (il s’agit de la valeur par défaut), l’espace de page dans le mode de mappage de texte de MM \_ équivaut à l’espace de l’appareil physique. La valeur de x augmente de gauche à droite. La valeur de y augmente de haut en bas. |
| MM \_ TWIPS       | Chaque unité de l’espace de page est mappée à un vingtième du point de l’imprimante (1/1440 de pouce). La valeur de x augmente de gauche à droite. La valeur de y augmente de bas en haut.                                                                                                                                           |



 

Pour définir un mode de mappage, appelez la fonction [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . Récupérez le mode de mappage actuel d’un contrôleur de périphérique en appelant la fonction [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode) .

Les transformations de l’espace de page aux espaces de l’appareil se composent de valeurs calculées à partir des points donnés par la fenêtre et la fenêtre d’affichage. Dans ce contexte, la fenêtre fait référence au système de coordonnées logiques de l’espace de la page, tandis que la fenêtre d’affichage fait référence au système de coordonnées de l’espace de l’appareil. La fenêtre et la fenêtre d’affichage comprennent chacune une origine, une étendue horizontale (« x ») et une étendue verticale (« y »). Les paramètres de fenêtre sont en coordonnées logiques. la fenêtre d’affichage en coordonnées de périphérique (pixels). Le système combine les origines et les étendues de la fenêtre et de la fenêtre d’affichage pour créer la transformation. Cela signifie que la fenêtre et la fenêtre d’affichage spécifient chacune la moitié des facteurs nécessaires à la définition de la transformation utilisée pour mapper les points de l’espace de page à l’espace de l’appareil. Ainsi, le système mappe l’origine de la fenêtre à l’origine de la fenêtre d’affichage et les étendues de fenêtre aux étendues de la fenêtre d’affichage, comme indiqué dans l’illustration suivante.

![Illustration montrant une origine de fenêtre dans l’espace de page et une origine de point de vue dans l’espace de l’appareil](images/cstrn-15.png)

Les extensions de fenêtre et de fenêtre d’affichage établissent un ratio ou un facteur d’échelle utilisé dans les transformations de l’espace de la page aux transformations de l’espace de l’appareil. Pour les six modes de mappage prédéfinis (MM \_ HIENGLISH, mm \_ LOENGLISH, mm \_ HIMETRIC, MM \_ LOMETRIC, mm \_ Text et mm \_ TWIPS), les étendues sont définies par le système lors de l’appel de [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) . Ils ne peuvent pas être modifiés. Les deux autres modes de mappage (MM \_ isotrope et mm \_ anisotrope) requièrent que les étendues soient spécifiées. Pour ce faire, appelez **SetMapMode** pour définir le mode approprié, puis appelez les fonctions [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex) et [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex) pour spécifier les étendues. Dans le mode de mappage de MM \_ isotropes, il est important d’appeler **SetWindowExtEx** avant d’appeler **SetViewportExtEx**.

Les origines de la fenêtre et de la fenêtre d’affichage établissent la traduction utilisée dans les transformations de l’espace de la page vers l’espace de l’appareil. Définissez les origines des fenêtres et des Viewports à l’aide des fonctions [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex) et [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . Les origines sont indépendantes des étendues, et une application peut les définir quel que soit le mode de mappage actuel. La modification d’un mode de mappage n’affecte pas les origines actuellement définies (même si cela peut affecter les étendues). Les origines sont spécifiées en unités absolues, ce qui n’est pas affecté par le mode de mappage actuel. Pour modifier les origines, utilisez les fonctions [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex) et [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex) .

La formule suivante montre les mathématiques impliquées dans la conversion d’un point de l’espace de page en espace de l’appareil.

``` syntax
Dx = ((Lx - WOx) * VEx / WEx) + VOx 
```

Les variables suivantes sont impliquées.

``` syntax
Dx     x value in device units 
Lx     x value in logical units (also known as page space units) 
WOx     window x origin 
VOx     viewport x origin 
WEx     window x-extent 
VEx     viewport x-extent 
```

La même équation avec y qui remplace x transforme le point de componentof y en un point.

La formule décale d’abord le point à partir de son origine de coordonnée. Cette valeur, qui n’est plus biaisée par l’origine, est ensuite mise à l’échelle dans le système de coordonnées de destination par le rapport entre les étendues. Enfin, la valeur mise à l’échelle est décalée de l’origine de destination vers son mappage final.

Les fonctions [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp) et [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp) peuvent être utilisées pour convertir des points logiques en points de périphérique et des points de périphérique en points logiques, respectivement.

 

 



