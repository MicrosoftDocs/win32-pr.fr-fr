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
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="8e678-104">Comment implémenter des info-bulles In-Place</span><span class="sxs-lookup"><span data-stu-id="8e678-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="8e678-105">Les info-bulles sur place sont utilisées pour afficher des chaînes de texte pour les objets qui ont été découpés.</span><span class="sxs-lookup"><span data-stu-id="8e678-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="8e678-106">Pour obtenir une illustration, consultez [à propos des contrôles ToolTip](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8e678-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="8e678-107">La différence entre les info-bulles ordinaires et sur place est le positionnement.</span><span class="sxs-lookup"><span data-stu-id="8e678-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="8e678-108">Par défaut, lorsque le pointeur de la souris est placé sur une région à laquelle une info-bulle est associée, l’info-bulle s’affiche à côté de la zone.</span><span class="sxs-lookup"><span data-stu-id="8e678-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="8e678-109">Toutefois, les info-bulles sont des fenêtres, et elles peuvent être positionnées partout où vous le souhaitez en appelant [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="8e678-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="8e678-110">La création d’une info-bulle sur place consiste à positionner la fenêtre d’info-bulle afin qu’elle recouvre la chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="8e678-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8e678-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="8e678-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8e678-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="8e678-112">Technologies</span></span>

-   [<span data-ttu-id="8e678-113">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="8e678-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8e678-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8e678-114">Prerequisites</span></span>

-   <span data-ttu-id="8e678-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="8e678-115">C/C++</span></span>
-   <span data-ttu-id="8e678-116">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="8e678-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8e678-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="8e678-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="8e678-118">Positionnement d’une info-bulle In-Place</span><span class="sxs-lookup"><span data-stu-id="8e678-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="8e678-119">Vous devez effectuer le suivi de trois rectangles lors du positionnement d’une info-bulle sur place :</span><span class="sxs-lookup"><span data-stu-id="8e678-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="8e678-120">Rectangle qui entoure le texte complet de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="8e678-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="8e678-121">Rectangle qui entoure le texte d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8e678-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="8e678-122">Le texte d’info-bulle est identique au texte complet de l’étiquette et est normalement de la même taille et de la même police.</span><span class="sxs-lookup"><span data-stu-id="8e678-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="8e678-123">Les deux rectangles de texte sont donc généralement de la même taille.</span><span class="sxs-lookup"><span data-stu-id="8e678-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="8e678-124">Rectangle de la fenêtre d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8e678-124">The tooltip window rectangle.</span></span> <span data-ttu-id="8e678-125">Ce rectangle est un peu plus grand que le rectangle de texte info-bulle qu’il englobe.</span><span class="sxs-lookup"><span data-stu-id="8e678-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="8e678-126">Les trois rectangles sont représentés schématiquement dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="8e678-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="8e678-127">La partie masquée du texte de l’étiquette est indiquée par un arrière-plan gris.</span><span class="sxs-lookup"><span data-stu-id="8e678-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![Diagramme montrant une longue chaîne, dont la moitié a un arrière-plan gris, puis la même chaîne dans un rectangle de fenêtre d’info-bulle plus grand](images/inplace.png)

<span data-ttu-id="8e678-129">Pour créer une info-bulle sur place, vous devez positionner le rectangle du texte de l’info-bulle afin qu’il recouvre le rectangle du texte de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="8e678-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="8e678-130">La procédure d’alignement des deux rectangles est relativement simple :</span><span class="sxs-lookup"><span data-stu-id="8e678-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="8e678-131">Définissez le rectangle du texte de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="8e678-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="8e678-132">Positionnez la fenêtre d’info-bulle afin que le rectangle de texte de l’info-bulle recouvre le rectangle du texte de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="8e678-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="8e678-133">Dans la pratique, il est généralement suffisant d’aligner l’angle supérieur gauche des deux rectangles de texte.</span><span class="sxs-lookup"><span data-stu-id="8e678-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="8e678-134">Toute tentative de redimensionnement du rectangle d’info-bulle pour qu’il corresponde exactement au rectangle de texte de l’étiquette peut entraîner des problèmes avec l’affichage de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8e678-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="8e678-135">Le problème de ce schéma simple est que vous ne pouvez pas positionner le rectangle de texte info-bulle directement.</span><span class="sxs-lookup"><span data-stu-id="8e678-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="8e678-136">Au lieu de cela, vous devez positionner le rectangle de la fenêtre d’info-bulle juste au-dessus et à gauche du rectangle de texte de l’étiquette afin que les angles des deux rectangles de texte coïncident.</span><span class="sxs-lookup"><span data-stu-id="8e678-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="8e678-137">En d’autres termes, vous devez connaître le décalage entre le rectangle de la fenêtre d’info-bulle et le rectangle de texte délimité.</span><span class="sxs-lookup"><span data-stu-id="8e678-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="8e678-138">En général, il n’existe aucun moyen simple de déterminer ce décalage.</span><span class="sxs-lookup"><span data-stu-id="8e678-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="8e678-139">Implémenter des info-bulles In-Place</span><span class="sxs-lookup"><span data-stu-id="8e678-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="8e678-140">Le fragment de code suivant illustre l’utilisation d’un message [**atténuation \_ ADJUSTRECT**](ttm-adjustrect.md) dans un gestionnaire d' [ \_ affichage ttn](ttn-show.md) pour afficher une info-bulle sur place.</span><span class="sxs-lookup"><span data-stu-id="8e678-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="8e678-141">Votre application indique que le texte de l’étiquette est tronqué en affectant à la variable Private *fMyStringIsTruncated* la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="8e678-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="8e678-142">Le gestionnaire appelle une fonction définie par l’application, **GetMyItemRect**, pour récupérer le rectangle du texte de l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="8e678-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="8e678-143">Ce rectangle est passé au contrôle ToolTip avec **atténuation \_ ADJUSTRECT**, qui retourne le rectangle de fenêtre correspondant.</span><span class="sxs-lookup"><span data-stu-id="8e678-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="8e678-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) est ensuite appelé pour positionner l’info-bulle sur l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="8e678-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


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



<span data-ttu-id="8e678-145">Cet exemple ne modifie pas la taille de l’info-bulle, mais simplement sa position.</span><span class="sxs-lookup"><span data-stu-id="8e678-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="8e678-146">Les deux rectangles de texte sont alignés sur les angles supérieurs gauches, mais pas nécessairement avec les mêmes dimensions.</span><span class="sxs-lookup"><span data-stu-id="8e678-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="8e678-147">Dans la pratique, la différence est généralement petite, et cette approche est recommandée dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="8e678-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="8e678-148">Bien que vous puissiez, en principe, utiliser [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) pour redimensionner et repositionner l’info-bulle, cela peut avoir des conséquences imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="8e678-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e678-149">Notes</span><span class="sxs-lookup"><span data-stu-id="8e678-149">Remarks</span></span>

<span data-ttu-id="8e678-150">Les contrôles communs [version 5,80](common-control-versions.md) simplifient l’utilisation des info-bulles sur place par l’ajout d’un nouveau message, [**atténuation \_ ADJUSTRECT**](ttm-adjustrect.md).</span><span class="sxs-lookup"><span data-stu-id="8e678-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="8e678-151">Envoyez ce message avec les coordonnées du rectangle de texte de l’étiquette que vous souhaitez superposer à l’info-bulle et retourne les coordonnées d’un rectangle de fenêtre d’info-bulle positionné de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="8e678-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e678-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e678-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e678-153">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="8e678-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 