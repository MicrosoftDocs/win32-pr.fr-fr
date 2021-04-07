---
title: Comment implémenter des info-bulles
description: Les info-bulles sont similaires aux info-bulles standard, mais elles sont affichées dans un dessin animé \ 0034 ; bulle \ 0034 ; avec une tige pointant sur l’outil.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671978"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="95521-103">Comment implémenter des info-bulles</span><span class="sxs-lookup"><span data-stu-id="95521-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="95521-104">Les info-bulles sont similaires aux info-bulles standard, mais elles sont affichées dans un « ballon » de style dessin animé avec une tige pointant sur l’outil.</span><span class="sxs-lookup"><span data-stu-id="95521-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="95521-105">Les info-bulles peuvent être à une seule ligne ou multiligne.</span><span class="sxs-lookup"><span data-stu-id="95521-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="95521-106">Elles sont créées et gérées à peu près de la même façon que les info-bulles standard.</span><span class="sxs-lookup"><span data-stu-id="95521-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="95521-107">La position par défaut du radical et du rectangle est indiquée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="95521-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="95521-108">Si l’outil est trop près du haut de l’écran, l’info-bulle apparaît en dessous et à droite du rectangle de l’outil.</span><span class="sxs-lookup"><span data-stu-id="95521-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="95521-109">Si l’outil est trop près du côté droit de l’écran, des principes similaires s’appliquent, mais l’info-bulle apparaît à gauche du rectangle de l’outil.</span><span class="sxs-lookup"><span data-stu-id="95521-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![capture d’écran d’une boîte de dialogue ; une info-bulle avec une ligne de texte s’affiche au-dessus et à droite de la cible.](images/tt-balloon.png)

<span data-ttu-id="95521-111">Vous pouvez modifier le positionnement par défaut en définissant l’indicateur **ttf \_ CENTERTIP** dans le membre **UFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="95521-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="95521-112">Dans ce cas, le radical pointe normalement vers le centre du bord inférieur du rectangle de l’outil, et le rectangle de texte s’affiche directement sous l’outil.</span><span class="sxs-lookup"><span data-stu-id="95521-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="95521-113">Le radical est attaché au rectangle de texte au centre du bord supérieur.</span><span class="sxs-lookup"><span data-stu-id="95521-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="95521-114">Si l’outil est trop près du bas de l’écran, le rectangle de texte est centré au-dessus de l’outil, et le pédoncule est attaché au centre du bord inférieur.</span><span class="sxs-lookup"><span data-stu-id="95521-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="95521-115">L’illustration suivante montre une info-bulle centrée sur l’outil.</span><span class="sxs-lookup"><span data-stu-id="95521-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![capture d’écran d’une boîte de dialogue ; une info-bulle avec une ligne de texte s’affiche centrée sous la cible](images/tt-ballooncenter.png)

<span data-ttu-id="95521-117">Si vous souhaitez spécifier l’emplacement des points de séquence, définissez l’indicateur de **\_ suivi ttf** dans le membre **UFlags** de la structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="95521-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="95521-118">Vous spécifiez ensuite la coordonnée en envoyant un message [**atténuation \_ TRACKPOSITION**](ttm-trackposition.md) , avec les coordonnées x et y dans la valeur *lParam* .</span><span class="sxs-lookup"><span data-stu-id="95521-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="95521-119">Si **ttf \_ CENTERTIP** est également défini, la tige pointe toujours vers la position spécifiée par le message **atténuation \_ TRACKPOSITION** .</span><span class="sxs-lookup"><span data-stu-id="95521-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="95521-120">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="95521-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="95521-121">Technologies</span><span class="sxs-lookup"><span data-stu-id="95521-121">Technologies</span></span>

-   [<span data-ttu-id="95521-122">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="95521-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="95521-123">Prérequis</span><span class="sxs-lookup"><span data-stu-id="95521-123">Prerequisites</span></span>

-   <span data-ttu-id="95521-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="95521-124">C/C++</span></span>
-   <span data-ttu-id="95521-125">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="95521-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="95521-126">Instructions</span><span class="sxs-lookup"><span data-stu-id="95521-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="95521-127">Implémenter des info-bulles</span><span class="sxs-lookup"><span data-stu-id="95521-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="95521-128">L’exemple de code suivant montre comment implémenter une info-bulle centrée à l’aide du style de contrôle ToolTip info-bulle **TTS \_** .</span><span class="sxs-lookup"><span data-stu-id="95521-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95521-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95521-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95521-130">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="95521-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="95521-131">**Styles d’info-bulle**</span><span class="sxs-lookup"><span data-stu-id="95521-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




