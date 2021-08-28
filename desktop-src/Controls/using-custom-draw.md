---
title: Utilisation d’un dessin personnalisé
description: Cette section contient des exemples qui montrent comment implémenter un dessin personnalisé.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90cff5fd4d692d31b69c85980f872f3aca4504cad81a3439d0c4d31a4c73d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655869"
---
# <a name="using-custom-draw"></a>Utilisation d’un dessin personnalisé

Cette section contient des exemples qui montrent comment implémenter un dessin personnalisé.

Le fragment de code suivant est une partie d’un gestionnaire [**WM \_ Notify**](wm-notify.md) qui illustre comment gérer les notifications de dessin personnalisées envoyées à un contrôle List-View.


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



La première [notification \_ CUSTOMDRAW nm](nm-customdraw.md) a le membre **DwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) défini sur **CDDS \_ prépaint**. Le gestionnaire retourne [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) pour indiquer qu’il souhaite modifier un ou plusieurs éléments individuellement.

Si [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) a été retourné à l’étape précédente, la [notification \_ CUSTOMDRAW nm](nm-customdraw.md) suivante a **dwDrawStage** définie sur **CDDS \_ ITEMPREPAINT**. Le gestionnaire récupère les valeurs de couleur et de police actuelles. À ce stade, vous pouvez spécifier de nouvelles valeurs pour les modes petite icône, grande icône et liste. Si le contrôle est en mode rapport, vous pouvez également spécifier de nouvelles valeurs qui s’appliqueront à tous les sous-éléments de l’élément. Si vous n’avez rien modifié, retournez [**CDRF \_ NEWFONT**](cdrf-constants.md). Si le contrôle est en mode rapport et que vous souhaitez gérer les sous-éléments individuellement, retournez **CDRF \_ NOTIFYSUBITEMDRAW**.

La notification finale est envoyée uniquement si le contrôle est en mode rapport et si vous avez retourné **CDRF \_ NOTIFYSUBITEMDRAW** à l’étape précédente. La procédure de modification des polices et des couleurs est la même que celle de cette étape, mais elle ne s’applique qu’à un seul sous-élément. Retournez [**CDRF \_ NEWFONT**](cdrf-constants.md) pour notifier le contrôle si la couleur ou la police a été modifiée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[À propos du dessin personnalisé](about-custom-draw.md)
</dt> <dt>

[Référence de dessin personnalisée](custom-draw-reference.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[EXEMPLE : CustDTv illustre un dessin personnalisé dans un contrôle TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




