---
title: Message LVM_SETITEMCOUNT (commctrl. h)
description: Force le contrôle List-View à allouer de la mémoire pour le nombre spécifié d’éléments ou définit le nombre virtuel d’éléments dans un contrôle List-View virtuel.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e390e7ae5913053f91f7f2f8d197af1cf4b7a40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103228"
---
# <a name="lvm_setitemcount-message"></a><span data-ttu-id="acb17-104">\_Message SETITEMCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="acb17-104">LVM\_SETITEMCOUNT message</span></span>

<span data-ttu-id="acb17-105">Force le contrôle List-View à allouer de la mémoire pour le nombre spécifié d’éléments ou définit le nombre virtuel d’éléments dans un [contrôle List-View virtuel](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="acb17-105">Causes the list-view control to allocate memory for the specified number of items or sets the virtual number of items in a [virtual list-view control](list-view-controls-overview.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="acb17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acb17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acb17-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acb17-108">Nombre d’éléments que le contrôle List-View doit finalement contenir.</span><span class="sxs-lookup"><span data-stu-id="acb17-108">Number of items that the list-view control will ultimately contain.</span></span>

</dd> <dt>

<span data-ttu-id="acb17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acb17-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acb17-110">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="acb17-110">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="acb17-111">Valeurs qui spécifient le comportement du contrôle List View après la réinitialisation du nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="acb17-111">Values that specify the behavior of the list-view control after resetting the item count.</span></span> <span data-ttu-id="acb17-112">Cette valeur peut être une combinaison des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="acb17-112">This value can be a combination of the following:</span></span>



| <span data-ttu-id="acb17-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="acb17-113">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="acb17-114">Signification</span><span class="sxs-lookup"><span data-stu-id="acb17-114">Meaning</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <span data-ttu-id="acb17-115"><dt>**LVSICF \_ NOINVALIDATEALL**</dt></span><span class="sxs-lookup"><span data-stu-id="acb17-115"><dt>**LVSICF\_NOINVALIDATEALL**</dt></span></span> </dl> | <span data-ttu-id="acb17-116">Le contrôle de liste n’est pas redessiné à moins que les éléments affectés soient actuellement en vue.</span><span class="sxs-lookup"><span data-stu-id="acb17-116">The list-view control will not repaint unless affected items are currently in view.</span></span><br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <span data-ttu-id="acb17-117"><dt>**LVSICF \_ NOscroll**</dt></span><span class="sxs-lookup"><span data-stu-id="acb17-117"><dt>**LVSICF\_NOSCROLL**</dt></span></span> </dl>                      | <span data-ttu-id="acb17-118">Le contrôle List-View ne modifie pas la position de défilement lorsque le nombre d’éléments change.</span><span class="sxs-lookup"><span data-stu-id="acb17-118">The list-view control will not change the scroll position when the item count changes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb17-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acb17-119">Return value</span></span>

<span data-ttu-id="acb17-120">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="acb17-120">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb17-121">Notes</span><span class="sxs-lookup"><span data-stu-id="acb17-121">Remarks</span></span>

<span data-ttu-id="acb17-122">La façon dont la mémoire est allouée dépend de la façon dont le contrôle List-View a été créé.</span><span class="sxs-lookup"><span data-stu-id="acb17-122">How the memory is allocated depends on how the list-view control was created.</span></span> <span data-ttu-id="acb17-123">Vous pouvez envoyer ce message explicitement ou utiliser les macros [**ListView \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) ou [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) .</span><span class="sxs-lookup"><span data-stu-id="acb17-123">You can send this message explicitly or use the [**ListView\_SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) or [**ListView\_SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) macros.</span></span> <span data-ttu-id="acb17-124">Pour plus d’informations, consultez [Virtual List-View style](/windows/desktop/Controls/list-view-controls-overview).</span><span class="sxs-lookup"><span data-stu-id="acb17-124">For more information, see [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).</span></span>

<span data-ttu-id="acb17-125">Si le contrôle List-View a été créé sans le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) , l’envoi de ce message amène le contrôle à allouer ses structures de données internes pour le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="acb17-125">If the list-view control was created without the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, sending this message causes the control to allocate its internal data structures for the specified number of items.</span></span> <span data-ttu-id="acb17-126">Cela empêche le contrôle d’avoir à allouer les structures de données chaque fois qu’un élément est ajouté.</span><span class="sxs-lookup"><span data-stu-id="acb17-126">This prevents the control from having to allocate the data structures every time an item is added.</span></span>

<span data-ttu-id="acb17-127">Si le contrôle d’affichage de liste a été créé avec le style [**LVS \_ OWNERDATA**](list-view-window-styles.md) (un affichage de liste virtuel), l’envoi de ce message définit le nombre virtuel d’éléments que contient le contrôle.</span><span class="sxs-lookup"><span data-stu-id="acb17-127">If the list-view control was created with the [**LVS\_OWNERDATA**](list-view-window-styles.md) style (a virtual list view), sending this message sets the virtual number of items that the control contains.</span></span>

<span data-ttu-id="acb17-128">Le paramètre *lParam* est destiné uniquement aux contrôles List-View qui utilisent les styles [**LVS \_ OWNERDATA**](list-view-window-styles.md) et [**LVS \_**](list-view-window-styles.md) ou de [**\_ liste LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="acb17-128">The *lParam* parameter is intended only for list-view controls that use the [**LVS\_OWNERDATA**](list-view-window-styles.md) and [**LVS\_REPORT**](list-view-window-styles.md) or [**LVS\_LIST**](list-view-window-styles.md) styles.</span></span>

<span data-ttu-id="acb17-129">Lorsque l’affichage de liste de contrôle commun est une vue de liste virtualisée ([**LVS \_ OWNERDATA**](list-view-window-styles.md)), il existe une limite d’éléments de 100 millions dans la liste.</span><span class="sxs-lookup"><span data-stu-id="acb17-129">When the common control list-view is a virtualized list-view ([**LVS\_OWNERDATA**](list-view-window-styles.md)), there is a 100,000,000 item limit on the list-view.</span></span> <span data-ttu-id="acb17-130">Dans ce scénario, **LVM \_ SETITEMCOUNT** retourne false s’il a un *wParam* de 100 000 001.</span><span class="sxs-lookup"><span data-stu-id="acb17-130">In this scenario, **LVM\_SETITEMCOUNT** will return FALSE when it has a *wParam* of 100,000,001.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb17-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acb17-131">Requirements</span></span>



| <span data-ttu-id="acb17-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acb17-132">Requirement</span></span> | <span data-ttu-id="acb17-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="acb17-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acb17-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acb17-134">Minimum supported client</span></span><br/> | <span data-ttu-id="acb17-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acb17-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acb17-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acb17-136">Minimum supported server</span></span><br/> | <span data-ttu-id="acb17-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acb17-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acb17-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="acb17-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb17-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb17-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

