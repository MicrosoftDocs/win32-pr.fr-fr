---
title: Code de notification NM_CUSTOMDRAW (arborescence) (commctrl. h)
description: Envoyé par un contrôle Tree-View pour signaler à sa fenêtre parente les opérations de dessin. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (arborescence)
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843089"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="3eef4-105">\_Code de notification CUSTOMDRAW nm (arborescence)</span><span class="sxs-lookup"><span data-stu-id="3eef4-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="3eef4-106">Envoyé par un contrôle Tree-View pour signaler à sa fenêtre parente les opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="3eef4-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="3eef4-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3eef4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3eef4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eef4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eef4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3eef4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3eef4-110">Pointeur vers une structure [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) qui contient et reçoit des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="3eef4-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="3eef4-111">Le membre **dwItemSpec** du membre **NMCD** de cette structure contient le handle de l’élément qui est en train d’être dessiné.</span><span class="sxs-lookup"><span data-stu-id="3eef4-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="3eef4-112">Le membre **lItemlParam** du membre **NMCD** de cette structure contient le *lParam* de l’élément qui est en train d’être dessiné.</span><span class="sxs-lookup"><span data-stu-id="3eef4-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eef4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eef4-113">Return value</span></span>

<span data-ttu-id="3eef4-114">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="3eef4-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="3eef4-115">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="3eef4-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="3eef4-116">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3eef4-116">You must return one of the following values.</span></span>



| <span data-ttu-id="3eef4-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3eef4-117">Return code</span></span>                                                                                            | <span data-ttu-id="3eef4-118">Description</span><span class="sxs-lookup"><span data-stu-id="3eef4-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3eef4-119"><dt>**CDRF \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="3eef4-120">Le contrôle se dessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="3eef4-120">The control draws itself.</span></span> <span data-ttu-id="3eef4-121">Elle n’envoie pas de codes [ \_ CUSTOMDRAW nm](nm-customdraw.md) supplémentaires pour ce cycle de peinture.</span><span class="sxs-lookup"><span data-stu-id="3eef4-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="3eef4-122">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3eef4-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="3eef4-123"><dt>**CDRF \_ NOTIFYITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="3eef4-124">Le contrôle notifie le parent de toutes les opérations de dessin liées aux éléments.</span><span class="sxs-lookup"><span data-stu-id="3eef4-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="3eef4-125">Elle envoie les codes de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) avant et après les éléments de dessin.</span><span class="sxs-lookup"><span data-stu-id="3eef4-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="3eef4-126">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3eef4-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="3eef4-127"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="3eef4-128">Le contrôle avertit le parent après l’effacement d’un élément. Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3eef4-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="3eef4-129"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="3eef4-130">Le contrôle notifie le parent après avoir peint un élément.</span><span class="sxs-lookup"><span data-stu-id="3eef4-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="3eef4-131">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3eef4-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="3eef4-132"><dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="3eef4-133">Version 4,71.</span><span class="sxs-lookup"><span data-stu-id="3eef4-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="3eef4-134">Le contrôle notifie le parent lorsqu’un sous-élément de vue liste est en train d’être dessiné.</span><span class="sxs-lookup"><span data-stu-id="3eef4-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="3eef4-135">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="3eef4-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3eef4-136"><dt>**CDRF \_ NEWFONT**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="3eef4-137">Votre application a spécifié une nouvelle police pour l’élément. le contrôle utilise la nouvelle police.</span><span class="sxs-lookup"><span data-stu-id="3eef4-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="3eef4-138">Pour plus d’informations sur la modification des polices, consultez [modification des polices et des couleurs](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="3eef4-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="3eef4-139">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="3eef4-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="3eef4-140"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="3eef4-141">Votre application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="3eef4-141">Your application drew the item manually.</span></span> <span data-ttu-id="3eef4-142">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="3eef4-142">The control will not draw the item.</span></span> <span data-ttu-id="3eef4-143">Cela se produit lorsque **dwDrawStage** est égal à CDDS \_ ITEMPREPAINT.</span><span class="sxs-lookup"><span data-stu-id="3eef4-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="3eef4-144">Notes</span><span class="sxs-lookup"><span data-stu-id="3eef4-144">Remarks</span></span>

[<span data-ttu-id="3eef4-145">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="3eef4-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="3eef4-146">Si vous modifiez la police en retournant [**CDRF \_ NEWFONT**](cdrf-constants.md), le contrôle Tree-View peut afficher du texte tronqué.</span><span class="sxs-lookup"><span data-stu-id="3eef4-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="3eef4-147">Ce comportement est nécessaire pour la compatibilité descendante avec les versions antérieures des contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="3eef4-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="3eef4-148">Si vous souhaitez modifier la police d’un contrôle Tree-View, vous obtiendrez de meilleurs résultats si vous envoyez un message [**CCM \_ SETVERSION**](ccm-setversion.md) avec la valeur *wParam* définie sur 5 avant d’ajouter des éléments au contrôle.</span><span class="sxs-lookup"><span data-stu-id="3eef4-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eef4-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eef4-149">Requirements</span></span>



| <span data-ttu-id="3eef4-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eef4-150">Requirement</span></span> | <span data-ttu-id="3eef4-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eef4-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3eef4-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eef4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3eef4-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3eef4-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3eef4-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3eef4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3eef4-155">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3eef4-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3eef4-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="3eef4-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eef4-157"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eef4-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eef4-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eef4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eef4-159">Utilisation d’un dessin personnalisé</span><span class="sxs-lookup"><span data-stu-id="3eef4-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





