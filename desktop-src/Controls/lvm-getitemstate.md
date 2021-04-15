---
title: Message LVM_GETITEMSTATE (commctrl. h)
description: Récupère l’état d’un élément de vue liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetItemState.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466510"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="f4aa7-105">\_Message GETITEMSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="f4aa7-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="f4aa7-106">Récupère l’état d’un élément de vue liste.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="f4aa7-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="f4aa7-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4aa7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4aa7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4aa7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4aa7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4aa7-110">Index de l’élément de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="f4aa7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4aa7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4aa7-112">Informations d’État à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-112">State information to retrieve.</span></span> <span data-ttu-id="f4aa7-113">Ce paramètre peut être une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4aa7-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="f4aa7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4aa7-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="f4aa7-115">Signification</span><span class="sxs-lookup"><span data-stu-id="f4aa7-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="f4aa7-116"><dt>**LVIS \_ couper**</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="f4aa7-117">L’élément est marqué pour une opération couper-coller.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="f4aa7-118"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="f4aa7-119">L’élément est mis en surbrillance en tant que cible de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="f4aa7-120"><dt>**LVIS \_ concentré**</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="f4aa7-121">L’élément a le focus, donc il est entouré d’un rectangle de focus standard.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="f4aa7-122">Bien qu’un seul élément puisse être sélectionné, un seul élément peut avoir le focus.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="f4aa7-123"><dt>**LVIS \_ sélectionné**</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="f4aa7-124">L'élément est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-124">The item is selected.</span></span> <span data-ttu-id="f4aa7-125">L’apparence d’un élément sélectionné varie selon qu’il a le focus et également sur les couleurs système utilisées pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="f4aa7-126"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="f4aa7-127">Utilisez ce masque pour récupérer l’index de l’image de superposition de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="f4aa7-128"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="f4aa7-129">Utilisez ce masque pour récupérer l’index de l’image d’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4aa7-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4aa7-130">Return value</span></span>

<span data-ttu-id="f4aa7-131">Retourne l’état actuel de l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="f4aa7-132">Les seuls bits valides dans la valeur de retour sont ceux qui correspondent aux bits définis dans le paramètre *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f4aa7-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4aa7-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f4aa7-133">Remarks</span></span>

<span data-ttu-id="f4aa7-134">Les informations d’état d’un élément incluent un jeu d’indicateurs binaires, ainsi que des index de liste d’images qui indiquent l’image d’état de l’élément et l’image de superposition.</span><span class="sxs-lookup"><span data-stu-id="f4aa7-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4aa7-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4aa7-135">Requirements</span></span>



| <span data-ttu-id="f4aa7-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4aa7-136">Requirement</span></span> | <span data-ttu-id="f4aa7-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4aa7-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4aa7-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4aa7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f4aa7-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4aa7-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4aa7-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4aa7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f4aa7-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4aa7-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4aa7-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4aa7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4aa7-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4aa7-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4aa7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4aa7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4aa7-145">**\_SETITEMSTATE LVM**</span><span class="sxs-lookup"><span data-stu-id="f4aa7-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 





