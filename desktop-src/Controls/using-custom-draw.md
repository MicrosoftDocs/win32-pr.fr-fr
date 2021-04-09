---
title: Utilisation d’un dessin personnalisé
description: Cette section contient des exemples qui montrent comment implémenter un dessin personnalisé.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104030862"
---
# <a name="using-custom-draw"></a><span data-ttu-id="67a1c-103">Utilisation d’un dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="67a1c-103">Using Custom Draw</span></span>

<span data-ttu-id="67a1c-104">Cette section contient des exemples qui montrent comment implémenter un dessin personnalisé.</span><span class="sxs-lookup"><span data-stu-id="67a1c-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="67a1c-105">Le fragment de code suivant est une partie d’un gestionnaire [**WM \_ Notify**](wm-notify.md) qui illustre comment gérer les notifications de dessin personnalisées envoyées à un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="67a1c-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


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



<span data-ttu-id="67a1c-106">La première [notification \_ CUSTOMDRAW nm](nm-customdraw.md) a le membre **DwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) défini sur **CDDS \_ prépaint**.</span><span class="sxs-lookup"><span data-stu-id="67a1c-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="67a1c-107">Le gestionnaire retourne [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) pour indiquer qu’il souhaite modifier un ou plusieurs éléments individuellement.</span><span class="sxs-lookup"><span data-stu-id="67a1c-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="67a1c-108">Si [**CDRF \_ NOTIFYITEMDRAW**](cdrf-constants.md) a été retourné à l’étape précédente, la [notification \_ CUSTOMDRAW nm](nm-customdraw.md) suivante a **dwDrawStage** définie sur **CDDS \_ ITEMPREPAINT**.</span><span class="sxs-lookup"><span data-stu-id="67a1c-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="67a1c-109">Le gestionnaire récupère les valeurs de couleur et de police actuelles.</span><span class="sxs-lookup"><span data-stu-id="67a1c-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="67a1c-110">À ce stade, vous pouvez spécifier de nouvelles valeurs pour les modes petite icône, grande icône et liste.</span><span class="sxs-lookup"><span data-stu-id="67a1c-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="67a1c-111">Si le contrôle est en mode rapport, vous pouvez également spécifier de nouvelles valeurs qui s’appliqueront à tous les sous-éléments de l’élément.</span><span class="sxs-lookup"><span data-stu-id="67a1c-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="67a1c-112">Si vous n’avez rien modifié, retournez [**CDRF \_ NEWFONT**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="67a1c-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="67a1c-113">Si le contrôle est en mode rapport et que vous souhaitez gérer les sous-éléments individuellement, retournez **CDRF \_ NOTIFYSUBITEMDRAW**.</span><span class="sxs-lookup"><span data-stu-id="67a1c-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="67a1c-114">La notification finale est envoyée uniquement si le contrôle est en mode rapport et si vous avez retourné **CDRF \_ NOTIFYSUBITEMDRAW** à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="67a1c-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="67a1c-115">La procédure de modification des polices et des couleurs est la même que celle de cette étape, mais elle ne s’applique qu’à un seul sous-élément.</span><span class="sxs-lookup"><span data-stu-id="67a1c-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="67a1c-116">Retournez [**CDRF \_ NEWFONT**](cdrf-constants.md) pour notifier le contrôle si la couleur ou la police a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="67a1c-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67a1c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="67a1c-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="67a1c-118">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="67a1c-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="67a1c-119">À propos du dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="67a1c-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="67a1c-120">Référence de dessin personnalisée</span><span class="sxs-lookup"><span data-stu-id="67a1c-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="67a1c-121">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="67a1c-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="67a1c-122">EXEMPLE : CustDTv illustre un dessin personnalisé dans un contrôle TreeView (Q248496)</span><span class="sxs-lookup"><span data-stu-id="67a1c-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




