---
title: Message TBM_GETSELEND (commctrl. h)
description: Récupère la position de fin de la plage de sélection actuelle dans un TrackBar.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- TBM_GETSELEND les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465366"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="bf971-104">\_Message TBM GETSELEND</span><span class="sxs-lookup"><span data-stu-id="bf971-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="bf971-105">Récupère la position de fin de la plage de sélection actuelle dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bf971-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf971-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf971-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf971-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf971-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bf971-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bf971-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bf971-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf971-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bf971-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bf971-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf971-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf971-111">Return value</span></span>

<span data-ttu-id="bf971-112">Retourne une valeur 32 bits qui spécifie la position de fin de la plage de sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="bf971-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf971-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf971-113">Remarks</span></span>

<span data-ttu-id="bf971-114">Un TrackBar ne peut avoir une plage de sélection que si vous avez spécifié le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) quand vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="bf971-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf971-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf971-115">Requirements</span></span>



| <span data-ttu-id="bf971-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf971-116">Requirement</span></span> | <span data-ttu-id="bf971-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf971-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf971-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf971-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf971-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf971-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf971-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf971-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf971-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf971-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf971-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf971-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf971-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf971-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf971-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf971-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf971-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bf971-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bf971-126">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="bf971-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="bf971-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="bf971-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="bf971-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="bf971-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="bf971-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="bf971-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





