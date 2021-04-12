---
title: NM_CUSTOMDRAW le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle des opérations de dessin personnalisées. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464267"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="05b89-105">\_Code de notification CUSTOMDRAW nm</span><span class="sxs-lookup"><span data-stu-id="05b89-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="05b89-106">Avertit la fenêtre parente d’un contrôle des opérations de dessin personnalisées.</span><span class="sxs-lookup"><span data-stu-id="05b89-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="05b89-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="05b89-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="05b89-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05b89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05b89-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05b89-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05b89-110">Pointeur vers une structure de dessin personnalisée qui contient des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="05b89-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="05b89-111">La liste suivante spécifie les contrôles et leurs structures associées.</span><span class="sxs-lookup"><span data-stu-id="05b89-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="05b89-112">Contrôler</span><span class="sxs-lookup"><span data-stu-id="05b89-112">Control</span></span>                     | <span data-ttu-id="05b89-113">Structure de dessin personnalisée</span><span class="sxs-lookup"><span data-stu-id="05b89-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="05b89-114">Rebar, TrackBar et en-tête</span><span class="sxs-lookup"><span data-stu-id="05b89-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="05b89-115">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="05b89-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="05b89-116">Affichage Liste</span><span class="sxs-lookup"><span data-stu-id="05b89-116">List view</span></span>                   | [<span data-ttu-id="05b89-117">**NMLVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="05b89-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="05b89-118">Info-bulle</span><span class="sxs-lookup"><span data-stu-id="05b89-118">Tooltip</span></span>                     | [<span data-ttu-id="05b89-119">**NMTTCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="05b89-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="05b89-120">Arborescence</span><span class="sxs-lookup"><span data-stu-id="05b89-120">Tree view</span></span>                   | [<span data-ttu-id="05b89-121">**NMTVCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="05b89-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="05b89-122">Barre d’outils</span><span class="sxs-lookup"><span data-stu-id="05b89-122">Toolbar</span></span>                     | [<span data-ttu-id="05b89-123">**NMTBCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="05b89-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05b89-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05b89-124">Return value</span></span>

<span data-ttu-id="05b89-125">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="05b89-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="05b89-126">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="05b89-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="05b89-127">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="05b89-127">You must return one of the following values.</span></span>



| <span data-ttu-id="05b89-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="05b89-128">Return code</span></span>                                                                                            | <span data-ttu-id="05b89-129">Description</span><span class="sxs-lookup"><span data-stu-id="05b89-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05b89-130"><dt>**CDRF \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="05b89-131">Le contrôle se dessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="05b89-131">The control will draw itself.</span></span> <span data-ttu-id="05b89-132">Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture.</span><span class="sxs-lookup"><span data-stu-id="05b89-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="05b89-133">Cet indicateur ne peut pas être utilisé avec un autre indicateur.</span><span class="sxs-lookup"><span data-stu-id="05b89-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="05b89-134"><dt>**CDRF, \_ INerase**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="05b89-135">Le contrôle dessinera uniquement l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="05b89-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="05b89-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="05b89-137">Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="05b89-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="05b89-138">Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="05b89-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="05b89-139">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="05b89-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="05b89-140"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="05b89-141">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="05b89-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="05b89-142">Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="05b89-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="05b89-143">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="05b89-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="05b89-144"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="05b89-145">Le contrôle notifie le parent après l’effacement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="05b89-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="05b89-146">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="05b89-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="05b89-147"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="05b89-148">Le contrôle enverra un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) lorsque le cycle de peinture de l’ensemble du contrôle est terminé.</span><span class="sxs-lookup"><span data-stu-id="05b89-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="05b89-149">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="05b89-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="05b89-150"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="05b89-151">Votre application recevra un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avec **dwDrawStage** défini sur CDDS \_ ITEMPREPAINT CDDS sous- \| \_ élément avant que chaque sous-élément de vue liste soit dessiné.</span><span class="sxs-lookup"><span data-stu-id="05b89-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="05b89-152">Vous pouvez ensuite spécifier la police et la couleur de chaque sous-élément séparément ou retourner [**CDRF \_ par défaut**](cdrf-constants.md) pour le traitement par défaut.</span><span class="sxs-lookup"><span data-stu-id="05b89-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="05b89-153">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="05b89-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="05b89-154"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="05b89-155">Votre application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="05b89-155">Your application drew the item manually.</span></span> <span data-ttu-id="05b89-156">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="05b89-156">The control will not draw the item.</span></span> <span data-ttu-id="05b89-157">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="05b89-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="05b89-158"><dt>**CDRF \_ SKIPPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="05b89-159">Le contrôle ne dessine pas le rectangle de focus autour d’un élément.</span><span class="sxs-lookup"><span data-stu-id="05b89-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="05b89-160">Notes</span><span class="sxs-lookup"><span data-stu-id="05b89-160">Remarks</span></span>

<span data-ttu-id="05b89-161">Actuellement, les contrôles suivants prennent en charge la fonctionnalité de dessin personnalisée : en-tête, mode liste, rebar, barre d’outils, info-bulle, TrackBar et arborescence.</span><span class="sxs-lookup"><span data-stu-id="05b89-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="05b89-162">Le dessin personnalisé est également pris en charge pour les contrôles Button si vous disposez d’un manifeste d’application pour vous assurer que Comctl32.dll version 6 est disponible.</span><span class="sxs-lookup"><span data-stu-id="05b89-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="05b89-163">Si ce message est géré dans une procédure de dialogue, vous devez définir la valeur de retour dans le cadre des données de la fenêtre avant de retourner la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="05b89-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="05b89-164">Pour plus d’informations, consultez [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span><span class="sxs-lookup"><span data-stu-id="05b89-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="05b89-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05b89-165">Requirements</span></span>



| <span data-ttu-id="05b89-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05b89-166">Requirement</span></span> | <span data-ttu-id="05b89-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="05b89-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05b89-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05b89-168">Minimum supported client</span></span><br/> | <span data-ttu-id="05b89-169">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05b89-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05b89-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05b89-170">Minimum supported server</span></span><br/> | <span data-ttu-id="05b89-171">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05b89-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05b89-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="05b89-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="05b89-173"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05b89-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05b89-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05b89-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="05b89-175">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="05b89-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05b89-176">Dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="05b89-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

