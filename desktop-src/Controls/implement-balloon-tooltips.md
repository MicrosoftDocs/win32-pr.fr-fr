---
title: Comment implémenter des info-bulles
description: Les info-bulles sont similaires aux info-bulles standard, mais elles sont affichées dans un dessin animé \ 0034 ; bulle \ 0034 ; avec une tige pointant sur l’outil.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999899"
---
# <a name="how-to-implement-balloon-tooltips"></a>Comment implémenter des info-bulles

Les info-bulles sont similaires aux info-bulles standard, mais elles sont affichées dans un « ballon » de style dessin animé avec une tige pointant sur l’outil. Les info-bulles peuvent être à une seule ligne ou multiligne. Elles sont créées et gérées à peu près de la même façon que les info-bulles standard.

La position par défaut du radical et du rectangle est indiquée dans l’illustration suivante. Si l’outil est trop près du haut de l’écran, l’info-bulle apparaît en dessous et à droite du rectangle de l’outil. Si l’outil est trop près du côté droit de l’écran, des principes similaires s’appliquent, mais l’info-bulle apparaît à gauche du rectangle de l’outil.

![capture d’écran d’une boîte de dialogue ; une info-bulle avec une ligne de texte s’affiche au-dessus et à droite de la cible.](images/tt-balloon.png)

Vous pouvez modifier le positionnement par défaut en définissant l’indicateur **ttf \_ CENTERTIP** dans le membre **UFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle. Dans ce cas, le radical pointe normalement vers le centre du bord inférieur du rectangle de l’outil, et le rectangle de texte s’affiche directement sous l’outil. Le radical est attaché au rectangle de texte au centre du bord supérieur. Si l’outil est trop près du bas de l’écran, le rectangle de texte est centré au-dessus de l’outil, et le pédoncule est attaché au centre du bord inférieur.

L’illustration suivante montre une info-bulle centrée sur l’outil.

![capture d’écran d’une boîte de dialogue ; une info-bulle avec une ligne de texte s’affiche centrée sous la cible](images/tt-ballooncenter.png)

Si vous souhaitez spécifier l’emplacement des points de séquence, définissez l’indicateur de **\_ suivi ttf** dans le membre **UFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle. Vous spécifiez ensuite la coordonnée en envoyant un message [**atténuation \_ TRACKPOSITION**](ttm-trackposition.md) , avec les coordonnées x et y dans la valeur *lParam* . Si **ttf \_ CENTERTIP** est également défini, la tige pointe toujours vers la position spécifiée par le message **atténuation \_ TRACKPOSITION** .

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="implement-balloon-tooltips"></a>Implémenter des info-bulles

L’exemple de code suivant montre comment implémenter une info-bulle centrée à l’aide du style de contrôle ToolTip info-bulle **TTS \_** .


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> <dt>

[**Styles d’info-bulle**](tooltip-styles.md)
</dt> </dl>

 

 




