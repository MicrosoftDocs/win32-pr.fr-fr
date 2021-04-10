---
title: Code de notification NM_CUSTOMDRAW (Rebar) (commctrl. h)
description: Envoyé par le contrôle rebar pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (Rebar)
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106624"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="84577-105">\_Code de notification CUSTOMDRAW nm (Rebar)</span><span class="sxs-lookup"><span data-stu-id="84577-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="84577-106">Envoyé par le contrôle rebar pour signaler à sa fenêtre parente les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="84577-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="84577-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="84577-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="84577-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84577-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84577-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84577-110">Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="84577-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="84577-111">Le membre **dwItemSpec** de cette structure contient l’identificateur de la bande en cours de dessin.</span><span class="sxs-lookup"><span data-stu-id="84577-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="84577-112">Le membre **lItemlParam** de cette structure contient le *lParam* de la bande qui est dessinée.</span><span class="sxs-lookup"><span data-stu-id="84577-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84577-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84577-113">Return value</span></span>

<span data-ttu-id="84577-114">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="84577-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="84577-115">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="84577-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="84577-116">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="84577-116">You must return one of the following values.</span></span>



| <span data-ttu-id="84577-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="84577-117">Return code</span></span>                                                                                            | <span data-ttu-id="84577-118">Description</span><span class="sxs-lookup"><span data-stu-id="84577-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84577-119"><dt>**CDRF \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="84577-120">Le contrôle se dessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="84577-120">The control will draw itself.</span></span> <span data-ttu-id="84577-121">Il n’enverra pas de notifications [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture.</span><span class="sxs-lookup"><span data-stu-id="84577-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="84577-122">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="84577-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="84577-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="84577-124">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="84577-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="84577-125">Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="84577-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="84577-126">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="84577-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="84577-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="84577-128">Le contrôle notifie le parent après l’effacement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="84577-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="84577-129">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="84577-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="84577-130"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="84577-131">Le contrôle notifie le parent après avoir peint un élément.</span><span class="sxs-lookup"><span data-stu-id="84577-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="84577-132">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="84577-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="84577-133"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="84577-134">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="84577-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="84577-135">Il envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="84577-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="84577-136">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="84577-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="84577-137"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="84577-138">L’application a spécifié une nouvelle police pour l’élément ; le contrôle utilise la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="84577-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="84577-139">Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="84577-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="84577-140">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="84577-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="84577-141"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="84577-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="84577-142">L’application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="84577-142">The application drew the item manually.</span></span> <span data-ttu-id="84577-143">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="84577-143">The control will not draw the item.</span></span> <span data-ttu-id="84577-144">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="84577-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="84577-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84577-145">Requirements</span></span>



| <span data-ttu-id="84577-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84577-146">Requirement</span></span> | <span data-ttu-id="84577-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="84577-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84577-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84577-148">Minimum supported client</span></span><br/> | <span data-ttu-id="84577-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84577-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84577-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84577-150">Minimum supported server</span></span><br/> | <span data-ttu-id="84577-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84577-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84577-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="84577-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="84577-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84577-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84577-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84577-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84577-155">Utilisation d’un dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="84577-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





