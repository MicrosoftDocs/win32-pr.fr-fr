---
title: Message SBM_SETRANGEREDRAW (winuser. h)
description: Une application envoie le \_ message SBM SETRANGEREDRAW à un contrôle de barre de défilement pour définir les valeurs de position minimale et maximale et pour redessiner le contrôle.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW les contrôles de message Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032342"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="78332-104">\_Message SBM SETRANGEREDRAW</span><span class="sxs-lookup"><span data-stu-id="78332-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="78332-105">Une application envoie le message **SBM \_ SETRANGEREDRAW** à un contrôle de barre de défilement pour définir les valeurs de position minimale et maximale et pour redessiner le contrôle.</span><span class="sxs-lookup"><span data-stu-id="78332-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="78332-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78332-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78332-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78332-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78332-108">Spécifie la position de défilement minimale.</span><span class="sxs-lookup"><span data-stu-id="78332-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="78332-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78332-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78332-110">Spécifie la position de défilement maximale.</span><span class="sxs-lookup"><span data-stu-id="78332-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78332-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78332-111">Return value</span></span>

<span data-ttu-id="78332-112">**ComCtl32.dll version 5,0**: si la position de la case de défilement a changé, la valeur de retour est la position précédente de la case de défilement ; dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="78332-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="78332-113">**ComCtl32.dll version 6,0**: position actuelle de la case de défilement, qu’elle ait été modifiée ou non.</span><span class="sxs-lookup"><span data-stu-id="78332-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="78332-114">Notes</span><span class="sxs-lookup"><span data-stu-id="78332-114">Remarks</span></span>

<span data-ttu-id="78332-115">Les valeurs par défaut de la position minimale et maximale sont égales à zéro.</span><span class="sxs-lookup"><span data-stu-id="78332-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="78332-116">La différence entre les valeurs spécifiées par les paramètres *wParam* et *lParam* ne doit pas être supérieure à MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="78332-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="78332-117">Si les valeurs de position minimale et maximale sont égales, le contrôle de barre de défilement est masqué et, en fait, désactivé.</span><span class="sxs-lookup"><span data-stu-id="78332-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="78332-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78332-118">Requirements</span></span>



| <span data-ttu-id="78332-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78332-119">Requirement</span></span> | <span data-ttu-id="78332-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="78332-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78332-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78332-121">Minimum supported client</span></span><br/> | <span data-ttu-id="78332-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78332-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78332-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78332-123">Minimum supported server</span></span><br/> | <span data-ttu-id="78332-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78332-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78332-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="78332-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="78332-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78332-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78332-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78332-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="78332-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="78332-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78332-129">**\_GETPOS SBM**</span><span class="sxs-lookup"><span data-stu-id="78332-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="78332-130">**\_GETRANGE SBM**</span><span class="sxs-lookup"><span data-stu-id="78332-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="78332-131">**\_SetPos SBM**</span><span class="sxs-lookup"><span data-stu-id="78332-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="78332-132">**\_DÉtrange SBM**</span><span class="sxs-lookup"><span data-stu-id="78332-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





