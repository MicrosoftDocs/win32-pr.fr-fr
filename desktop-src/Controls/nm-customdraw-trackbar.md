---
title: Code de notification NM_CUSTOMDRAW (TrackBar) (commctrl. h)
description: Envoyé par un contrôle TrackBar pour notifier à ses fenêtres parentes les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- Contrôles Windows du code de notification NM_CUSTOMDRAW (TrackBar)
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
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106621"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="40ef8-105">\_Code de notification CUSTOMDRAW nm (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="40ef8-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="40ef8-106">Envoyé par un contrôle TrackBar pour notifier à ses fenêtres parentes les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="40ef8-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="40ef8-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="40ef8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="40ef8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40ef8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ef8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40ef8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40ef8-110">Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="40ef8-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="40ef8-111">Le membre **dwItemSpec** de cette structure contient une des valeurs de [dessin personnalisées](custom-draw-values.md) qui indique quelle partie du contrôle est dessinée.</span><span class="sxs-lookup"><span data-stu-id="40ef8-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="40ef8-112">Les contrôles TrackBar insèrent les valeurs suivantes dans le membre **dwItemSpec** de cette structure pour identifier la partie du contrôle qui est dessinée :</span><span class="sxs-lookup"><span data-stu-id="40ef8-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="40ef8-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="40ef8-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="40ef8-114">Signification</span><span class="sxs-lookup"><span data-stu-id="40ef8-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="40ef8-115"><dt>**\_canal TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="40ef8-116">Identifie le canal que le marqueur de curseur de défilement du contrôle TrackBar délimite.</span><span class="sxs-lookup"><span data-stu-id="40ef8-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="40ef8-117"><dt>**\_Thumb TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="40ef8-118">Identifie le marqueur de curseur de défilement du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="40ef8-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="40ef8-119">Il s’agit de la partie du contrôle qui est déplacée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="40ef8-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="40ef8-120"><dt>**TBCD \_ tics**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="40ef8-121">Identifie les graduations d’incrément qui apparaissent le long du bord du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="40ef8-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ef8-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40ef8-122">Return value</span></span>

<span data-ttu-id="40ef8-123">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="40ef8-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="40ef8-124">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="40ef8-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="40ef8-125">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="40ef8-125">You must return one of the following values.</span></span>



| <span data-ttu-id="40ef8-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="40ef8-126">Return code</span></span>                                                                                            | <span data-ttu-id="40ef8-127">Description</span><span class="sxs-lookup"><span data-stu-id="40ef8-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40ef8-128"><dt>**CDRF \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="40ef8-129">Le contrôle se dessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="40ef8-129">The control will draw itself.</span></span> <span data-ttu-id="40ef8-130">Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture.</span><span class="sxs-lookup"><span data-stu-id="40ef8-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="40ef8-131">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="40ef8-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="40ef8-132"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="40ef8-133">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="40ef8-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="40ef8-134">Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="40ef8-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="40ef8-135">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="40ef8-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="40ef8-136"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="40ef8-137">Le contrôle notifie le parent après l’effacement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="40ef8-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="40ef8-138">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="40ef8-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="40ef8-139"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="40ef8-140">Le contrôle notifie le parent après avoir peint un élément.</span><span class="sxs-lookup"><span data-stu-id="40ef8-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="40ef8-141">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="40ef8-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="40ef8-142"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="40ef8-143">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="40ef8-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="40ef8-144">Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en cours de dessin.</span><span class="sxs-lookup"><span data-stu-id="40ef8-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="40ef8-145">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="40ef8-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="40ef8-146"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="40ef8-147">Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="40ef8-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="40ef8-148">Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="40ef8-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="40ef8-149">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="40ef8-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="40ef8-150"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="40ef8-151">Votre application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="40ef8-151">Your application drew the item manually.</span></span> <span data-ttu-id="40ef8-152">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="40ef8-152">The control will not draw the item.</span></span> <span data-ttu-id="40ef8-153">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="40ef8-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="40ef8-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40ef8-154">Requirements</span></span>



| <span data-ttu-id="40ef8-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40ef8-155">Requirement</span></span> | <span data-ttu-id="40ef8-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="40ef8-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40ef8-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40ef8-157">Minimum supported client</span></span><br/> | <span data-ttu-id="40ef8-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40ef8-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40ef8-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40ef8-159">Minimum supported server</span></span><br/> | <span data-ttu-id="40ef8-160">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40ef8-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40ef8-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="40ef8-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="40ef8-162"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40ef8-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ef8-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40ef8-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ef8-164">Utilisation d’un dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="40ef8-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





