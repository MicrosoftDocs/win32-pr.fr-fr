---
title: Message TTM_TRACKACTIVATE (commctrl. h)
description: Active ou désactive une info-bulle de suivi.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- TTM_TRACKACTIVATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942374"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="ed48f-104">\_Message atténuation TRACKACTIVATE</span><span class="sxs-lookup"><span data-stu-id="ed48f-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="ed48f-105">Active ou désactive une info-bulle de suivi.</span><span class="sxs-lookup"><span data-stu-id="ed48f-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed48f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed48f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed48f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed48f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed48f-108">Valeur spécifiant si le suivi est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="ed48f-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="ed48f-109">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="ed48f-109">This value can be one of the following:</span></span>



| <span data-ttu-id="ed48f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed48f-110">Value</span></span>                                                                                                                                | <span data-ttu-id="ed48f-111">Signification</span><span class="sxs-lookup"><span data-stu-id="ed48f-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="ed48f-112"><dt>**:**</dt></span><span class="sxs-lookup"><span data-stu-id="ed48f-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="ed48f-113">Active le suivi.</span><span class="sxs-lookup"><span data-stu-id="ed48f-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="ed48f-114"><dt>**FAUSSES**</dt></span><span class="sxs-lookup"><span data-stu-id="ed48f-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="ed48f-115">Désactiver le suivi.</span><span class="sxs-lookup"><span data-stu-id="ed48f-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ed48f-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed48f-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed48f-117">Pointeur vers une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) qui identifie l’outil auquel ce message s’applique.</span><span class="sxs-lookup"><span data-stu-id="ed48f-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="ed48f-118">Les membres **HWND** et **UID** identifient l’outil, tandis que le membre **cbSize** spécifie la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="ed48f-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="ed48f-119">Tous les autres membres sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="ed48f-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed48f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed48f-120">Return value</span></span>

<span data-ttu-id="ed48f-121">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ed48f-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed48f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed48f-122">Requirements</span></span>



| <span data-ttu-id="ed48f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed48f-123">Requirement</span></span> | <span data-ttu-id="ed48f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed48f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed48f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed48f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ed48f-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed48f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed48f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed48f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ed48f-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed48f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed48f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ed48f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed48f-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed48f-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed48f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed48f-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed48f-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ed48f-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ed48f-133">**ATTÉNUATION \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="ed48f-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="ed48f-134">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ed48f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ed48f-135">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="ed48f-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





