---
title: Code de notification NM_CUSTOMDRAW (en-tête) (commctrl. h)
description: Envoyé par un contrôle header pour notifier sa fenêtre parente sur les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (en-tête)
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106544181"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="3402d-105">\_Code de notification CUSTOMDRAW nm (en-tête)</span><span class="sxs-lookup"><span data-stu-id="3402d-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="3402d-106">Envoyé par un contrôle header pour notifier sa fenêtre parente sur les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="3402d-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="3402d-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3402d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3402d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3402d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3402d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3402d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3402d-110">Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="3402d-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="3402d-111">Le membre **dwItemSpec** de cette structure contient l’index de l’élément qui est en train d’être dessiné et le membre **lItemlParam** de cette structure contient le *lParam* de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3402d-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3402d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3402d-112">Return value</span></span>

<span data-ttu-id="3402d-113">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="3402d-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="3402d-114">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="3402d-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="3402d-115">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3402d-115">You must return one of the following values.</span></span>



| <span data-ttu-id="3402d-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3402d-116">Return code</span></span>                                                                                            | <span data-ttu-id="3402d-117">Description</span><span class="sxs-lookup"><span data-stu-id="3402d-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3402d-118"><dt>**CDRF \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="3402d-119">Le contrôle se dessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="3402d-119">The control will draw itself.</span></span> <span data-ttu-id="3402d-120">Il n’enverra pas de messages [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture.</span><span class="sxs-lookup"><span data-stu-id="3402d-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="3402d-121">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3402d-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="3402d-122"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="3402d-123">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="3402d-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="3402d-124">Il envoie \_ les codes de notification CUSTOMDRAW nm avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="3402d-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="3402d-125">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3402d-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="3402d-126"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="3402d-127">Le contrôle notifie le parent après l’effacement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3402d-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="3402d-128">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3402d-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="3402d-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="3402d-130">Le contrôle notifie le parent après avoir peint un élément.</span><span class="sxs-lookup"><span data-stu-id="3402d-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="3402d-131">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3402d-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="3402d-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="3402d-133">[Versions de contrôle courantes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3402d-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="3402d-134">Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en cours de dessin.</span><span class="sxs-lookup"><span data-stu-id="3402d-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="3402d-135">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3402d-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="3402d-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="3402d-137">Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="3402d-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="3402d-138">Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="3402d-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="3402d-139">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="3402d-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="3402d-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="3402d-141">Votre application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="3402d-141">Your application drew the item manually.</span></span> <span data-ttu-id="3402d-142">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="3402d-142">The control will not draw the item.</span></span> <span data-ttu-id="3402d-143">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="3402d-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="3402d-144">Notes</span><span class="sxs-lookup"><span data-stu-id="3402d-144">Remarks</span></span>

<span data-ttu-id="3402d-145">Pour plus d’informations, consultez Utilisation d’un [dessin personnalisé](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="3402d-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="3402d-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3402d-146">Requirements</span></span>



| <span data-ttu-id="3402d-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3402d-147">Requirement</span></span> | <span data-ttu-id="3402d-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="3402d-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3402d-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3402d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3402d-150">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3402d-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3402d-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3402d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3402d-152">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3402d-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3402d-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="3402d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3402d-154"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3402d-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





