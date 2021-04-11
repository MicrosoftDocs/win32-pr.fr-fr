---
title: Message LVM_SETCALLBACKMASK (commctrl. h)
description: Modifie le masque de rappel pour un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetCallbackMask.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103364"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="0a9a9-105">\_Message SETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="0a9a9-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="0a9a9-106">Modifie le masque de rappel pour un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="0a9a9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="0a9a9-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a9a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a9a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a9a9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a9a9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a9a9-110">Valeur du masque de rappel.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-110">Value of the callback mask.</span></span> <span data-ttu-id="0a9a9-111">Les bits du masque indiquent les États ou images d’élément pour lesquels l’application stocke les données d’état actuelles.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="0a9a9-112">Cette valeur peut être n’importe quelle combinaison des constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a9a9-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="0a9a9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a9a9-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="0a9a9-114">Signification</span><span class="sxs-lookup"><span data-stu-id="0a9a9-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="0a9a9-115"><dt>**LVIS \_ couper**</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="0a9a9-116">L’élément est marqué pour une opération couper-coller.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="0a9a9-117"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="0a9a9-118">L’élément est mis en surbrillance en tant que cible de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="0a9a9-119"><dt>**LVIS \_ concentré**</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="0a9a9-120">L’élément a le focus.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="0a9a9-121"><dt>**LVIS \_ sélectionné**</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="0a9a9-122">L'élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="0a9a9-123"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="0a9a9-124">L’application stocke l’index de liste d’images de l’image de superposition actuelle pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="0a9a9-125"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="0a9a9-126">L’application stocke l’index de liste d’images de l’image d’État actuelle pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="0a9a9-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a9a9-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0a9a9-128">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a9a9-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a9a9-129">Return value</span></span>

<span data-ttu-id="0a9a9-130">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9a9-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0a9a9-131">Remarks</span></span>

<span data-ttu-id="0a9a9-132">Le *masque de rappel* d’un contrôle List-View est un jeu d’indicateurs binaires qui spécifient les États de l’élément pour lesquels l’application, plutôt que le contrôle, stocke les données actuelles.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="0a9a9-133">Le masque de rappel s’applique à tous les éléments du contrôle, contrairement à la désignation de l’élément de rappel, qui s’applique à un élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="0a9a9-134">Le masque de rappel a la valeur zéro par défaut, ce qui signifie que le contrôle List-View stocke toutes les informations sur l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="0a9a9-135">Après avoir créé un contrôle List-View et initialisé ses éléments, vous pouvez envoyer le **message \_ SETCALLBACKMASK LVM** pour modifier le masque de rappel.</span><span class="sxs-lookup"><span data-stu-id="0a9a9-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="0a9a9-136">Pour récupérer le masque de rappel actuel, envoyez le message [**\_ GETCALLBACKMASK LVM**](lvm-getcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="0a9a9-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="0a9a9-137">Pour plus d’informations sur les images de superposition et les images d’État, consultez [Ajout de listes d’images List-View](using-list-view-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0a9a9-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="0a9a9-138">Pour plus d’informations sur les rappels de vue de liste, consultez [éléments de rappel et masque de rappel](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a9a9-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9a9-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a9a9-139">Requirements</span></span>



| <span data-ttu-id="0a9a9-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a9a9-140">Requirement</span></span> | <span data-ttu-id="0a9a9-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a9a9-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a9a9-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a9a9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0a9a9-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a9a9-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a9a9-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a9a9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0a9a9-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a9a9-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a9a9-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a9a9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a9a9-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a9a9-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a9a9-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a9a9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a9a9-149">**LVN \_ GETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="0a9a9-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





