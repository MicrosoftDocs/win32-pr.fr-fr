---
title: Comment implémenter des info-bulles In-Place
description: Les info-bulles sur place sont utilisées pour afficher des chaînes de texte pour les objets qui ont été découpés. Pour obtenir une illustration, consultez à propos des contrôles ToolTip.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104032118"
---
# <a name="how-to-implement-in-place-tooltips"></a>Comment implémenter des info-bulles In-Place

Les info-bulles sur place sont utilisées pour afficher des chaînes de texte pour les objets qui ont été découpés. Pour obtenir une illustration, consultez [à propos des contrôles ToolTip](tooltip-controls.md).

La différence entre les info-bulles ordinaires et sur place est le positionnement. Par défaut, lorsque le pointeur de la souris est placé sur une région à laquelle une info-bulle est associée, l’info-bulle s’affiche à côté de la zone. Toutefois, les info-bulles sont des fenêtres, et elles peuvent être positionnées partout où vous le souhaitez en appelant [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). La création d’une info-bulle sur place consiste à positionner la fenêtre d’info-bulle afin qu’elle recouvre la chaîne de texte.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="positioning-an-in-place-tooltip"></a>Positionnement d’une info-bulle In-Place

Vous devez effectuer le suivi de trois rectangles lors du positionnement d’une info-bulle sur place :

1.  Rectangle qui entoure le texte complet de l’étiquette.
2.  Rectangle qui entoure le texte d’info-bulle. Le texte d’info-bulle est identique au texte complet de l’étiquette et est normalement de la même taille et de la même police. Les deux rectangles de texte sont donc généralement de la même taille.
3.  Rectangle de la fenêtre d’info-bulle. Ce rectangle est un peu plus grand que le rectangle de texte info-bulle qu’il englobe.


Les trois rectangles sont représentés schématiquement dans l’illustration suivante. La partie masquée du texte de l’étiquette est indiquée par un arrière-plan gris.

![Diagramme montrant une longue chaîne, dont la moitié a un arrière-plan gris, puis la même chaîne dans un rectangle de fenêtre d’info-bulle plus grand](images/inplace.png)

Pour créer une info-bulle sur place, vous devez positionner le rectangle du texte de l’info-bulle afin qu’il recouvre le rectangle du texte de l’étiquette. La procédure d’alignement des deux rectangles est relativement simple :

1.  Définissez le rectangle du texte de l’étiquette.
2.  Positionnez la fenêtre d’info-bulle afin que le rectangle de texte de l’info-bulle recouvre le rectangle du texte de l’étiquette.


Dans la pratique, il est généralement suffisant d’aligner l’angle supérieur gauche des deux rectangles de texte. Toute tentative de redimensionnement du rectangle d’info-bulle pour qu’il corresponde exactement au rectangle de texte de l’étiquette peut entraîner des problèmes avec l’affichage de l’info-bulle.

Le problème de ce schéma simple est que vous ne pouvez pas positionner le rectangle de texte info-bulle directement. Au lieu de cela, vous devez positionner le rectangle de la fenêtre d’info-bulle juste au-dessus et à gauche du rectangle de texte de l’étiquette afin que les angles des deux rectangles de texte coïncident. En d’autres termes, vous devez connaître le décalage entre le rectangle de la fenêtre d’info-bulle et le rectangle de texte délimité. En général, il n’existe aucun moyen simple de déterminer ce décalage.

### <a name="implement-in-place-tooltips"></a>Implémenter des info-bulles In-Place

Le fragment de code suivant illustre l’utilisation d’un message [**atténuation \_ ADJUSTRECT**](ttm-adjustrect.md) dans un gestionnaire d' [ \_ affichage ttn](ttn-show.md) pour afficher une info-bulle sur place. Votre application indique que le texte de l’étiquette est tronqué en affectant à la variable Private *fMyStringIsTruncated* la **valeur true**. Le gestionnaire appelle une fonction définie par l’application, **GetMyItemRect**, pour récupérer le rectangle du texte de l’étiquette. Ce rectangle est passé au contrôle ToolTip avec **atténuation \_ ADJUSTRECT**, qui retourne le rectangle de fenêtre correspondant. [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) est ensuite appelé pour positionner l’info-bulle sur l’étiquette.


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



Cet exemple ne modifie pas la taille de l’info-bulle, mais simplement sa position. Les deux rectangles de texte sont alignés sur les angles supérieurs gauches, mais pas nécessairement avec les mêmes dimensions. Dans la pratique, la différence est généralement petite, et cette approche est recommandée dans la plupart des cas. Bien que vous puissiez, en principe, utiliser [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour redimensionner et repositionner l’info-bulle, cela peut avoir des conséquences imprévisibles.

## <a name="remarks"></a>Notes

Les contrôles communs [version 5,80](common-control-versions.md) simplifient l’utilisation des info-bulles sur place par l’ajout d’un nouveau message, [**atténuation \_ ADJUSTRECT**](ttm-adjustrect.md). Envoyez ce message avec les coordonnées du rectangle de texte de l’étiquette que vous souhaitez superposer à l’info-bulle et retourne les coordonnées d’un rectangle de fenêtre d’info-bulle positionné de manière appropriée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 