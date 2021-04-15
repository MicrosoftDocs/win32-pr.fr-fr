---
title: Code de notification NM_CUSTOMDRAW (bouton) (commctrl. h)
description: Notifie la fenêtre parente d’un contrôle bouton sur les opérations de dessin personnalisées sur le bouton. Le contrôle Button envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Contrôles Windows de code de notification NM_CUSTOMDRAW (bouton)
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
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467114"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="92611-105">\_Code de notification CUSTOMDRAW nm (bouton)</span><span class="sxs-lookup"><span data-stu-id="92611-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="92611-106">Notifie la fenêtre parente d’un contrôle bouton sur les opérations de dessin personnalisées sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="92611-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="92611-107">Le contrôle Button envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="92611-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="92611-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92611-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92611-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92611-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92611-110">Pointeur vers une structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) qui contient des informations sur l’opération de dessin.</span><span class="sxs-lookup"><span data-stu-id="92611-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="92611-111">Le membre **dwItemSpec** de cette structure contient l’index de l’élément qui est en train d’être dessiné et le membre **lItemlParam** de cette structure contient le *lParam* de l’élément.</span><span class="sxs-lookup"><span data-stu-id="92611-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92611-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92611-112">Return value</span></span>

<span data-ttu-id="92611-113">La valeur que votre application peut retourner dépend de l’étape de dessin actuelle.</span><span class="sxs-lookup"><span data-stu-id="92611-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="92611-114">Le membre **dwDrawStage** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associée contient une valeur qui spécifie la phase de dessin.</span><span class="sxs-lookup"><span data-stu-id="92611-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="92611-115">Vous devez retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="92611-115">You must return one of the following values.</span></span>



| <span data-ttu-id="92611-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="92611-116">Return code</span></span>                                                                                          | <span data-ttu-id="92611-117">Description</span><span class="sxs-lookup"><span data-stu-id="92611-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92611-118"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="92611-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="92611-119">Le contrôle notifie le parent après l’effacement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="92611-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="92611-120">Cette valeur ne peut être utilisée que si **dwDrawStage** est égal à CDDS \_ preerase.</span><span class="sxs-lookup"><span data-stu-id="92611-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="92611-121"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="92611-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="92611-122">Le contrôle notifie le parent après avoir peint un élément.</span><span class="sxs-lookup"><span data-stu-id="92611-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="92611-123">Cela peut être utilisé uniquement si **dwDrawStage** est égal à CDDS \_ prépaint.</span><span class="sxs-lookup"><span data-stu-id="92611-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="92611-124"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="92611-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="92611-125">L’application a dessiné l’élément manuellement.</span><span class="sxs-lookup"><span data-stu-id="92611-125">The application drew the item manually.</span></span> <span data-ttu-id="92611-126">Le contrôle ne dessine pas l’élément.</span><span class="sxs-lookup"><span data-stu-id="92611-126">The control will not draw the item.</span></span> <span data-ttu-id="92611-127">Cela peut être utilisé lorsque **dwDrawStage** est égal à CDDS \_ PREerase ou CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="92611-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92611-128">Notes</span><span class="sxs-lookup"><span data-stu-id="92611-128">Remarks</span></span>

<span data-ttu-id="92611-129">Si le contrôle Button est marqué comme OwnerDraw (BS \_ OwnerDraw), le \_ Code de notification CUSTOMDRAW nm n’est pas envoyé.</span><span class="sxs-lookup"><span data-stu-id="92611-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="92611-130">Pour plus d’informations, consultez Utilisation d’un [dessin personnalisé](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="92611-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="92611-131">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="92611-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="92611-132">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="92611-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92611-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92611-133">Requirements</span></span>



| <span data-ttu-id="92611-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92611-134">Requirement</span></span> | <span data-ttu-id="92611-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="92611-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92611-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92611-136">Minimum supported client</span></span><br/> | <span data-ttu-id="92611-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92611-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="92611-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92611-138">Minimum supported server</span></span><br/> | <span data-ttu-id="92611-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92611-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="92611-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="92611-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="92611-141"><dt>Commctrl. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92611-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





