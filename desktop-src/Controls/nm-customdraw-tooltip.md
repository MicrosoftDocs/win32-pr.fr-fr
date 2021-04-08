---
title: Code de notification NM_CUSTOMDRAW (info-bulle) (commctrl. h)
description: Envoyé par un contrôle ToolTip pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (info-bulle)
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743980"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="a5a80-105">\_Code de notification CUSTOMDRAW nm (info-bulle)</span><span class="sxs-lookup"><span data-stu-id="a5a80-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="a5a80-106">Envoyé par un contrôle ToolTip pour signaler à sa fenêtre parente les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="a5a80-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="a5a80-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a5a80-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a5a80-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5a80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5a80-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5a80-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5a80-110">Pointeur vers une structure [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) qui contient des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="a5a80-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5a80-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5a80-111">Return value</span></span>

<span data-ttu-id="a5a80-112">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="a5a80-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="a5a80-113">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="a5a80-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="a5a80-114">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a5a80-114">You must return one of the following values.</span></span>



| <span data-ttu-id="a5a80-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a5a80-115">Return code</span></span>                                                                                            | <span data-ttu-id="a5a80-116">Description</span><span class="sxs-lookup"><span data-stu-id="a5a80-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5a80-117"><dt>**CDRF \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="a5a80-118">Le contrôle se dessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="a5a80-118">The control will draw itself.</span></span> <span data-ttu-id="a5a80-119">Il n’enverra pas de codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture.</span><span class="sxs-lookup"><span data-stu-id="a5a80-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="a5a80-120">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="a5a80-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="a5a80-121"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="a5a80-122">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="a5a80-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="a5a80-123">Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="a5a80-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="a5a80-124">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="a5a80-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="a5a80-125"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="a5a80-126">Le contrôle notifie le parent après l’effacement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="a5a80-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="a5a80-127">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="a5a80-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="a5a80-128"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="a5a80-129">Le contrôle notifie le parent après avoir peint un élément.</span><span class="sxs-lookup"><span data-stu-id="a5a80-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="a5a80-130">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="a5a80-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="a5a80-131"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="a5a80-132">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a5a80-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="a5a80-133">Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en cours de dessin.</span><span class="sxs-lookup"><span data-stu-id="a5a80-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="a5a80-134">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="a5a80-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="a5a80-135"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="a5a80-136">Votre application a spécifié une nouvelle police pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="a5a80-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="a5a80-137">Le contrôle utilise la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="a5a80-137">The control will use the new font.</span></span> <span data-ttu-id="a5a80-138">Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="a5a80-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="a5a80-139">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="a5a80-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="a5a80-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="a5a80-141">Votre application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="a5a80-141">Your application drew the item manually.</span></span> <span data-ttu-id="a5a80-142">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="a5a80-142">The control will not draw the item.</span></span> <span data-ttu-id="a5a80-143">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="a5a80-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="a5a80-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5a80-144">Requirements</span></span>



| <span data-ttu-id="a5a80-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5a80-145">Requirement</span></span> | <span data-ttu-id="a5a80-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5a80-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a80-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5a80-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a80-148">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5a80-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5a80-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5a80-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a80-150">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5a80-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5a80-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5a80-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5a80-152"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5a80-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a80-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5a80-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a80-154">Utilisation d’un dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="a5a80-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





