---
title: Message TBM_CLEARSEL (commctrl. h)
description: Efface la plage de sélection actuelle dans un TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- TBM_CLEARSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844438"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="57597-104">\_Message TBM CLEARSEL</span><span class="sxs-lookup"><span data-stu-id="57597-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="57597-105">Efface la plage de sélection actuelle dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="57597-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="57597-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57597-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57597-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57597-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="57597-108">Redraw flag.</span></span> <span data-ttu-id="57597-109">Si ce paramètre a la **valeur true**, le TrackBar est redessiné après l’effacement de la sélection.</span><span class="sxs-lookup"><span data-stu-id="57597-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="57597-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57597-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="57597-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="57597-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57597-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57597-112">Return value</span></span>

<span data-ttu-id="57597-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="57597-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57597-114">Notes</span><span class="sxs-lookup"><span data-stu-id="57597-114">Remarks</span></span>

<span data-ttu-id="57597-115">Un TrackBar ne peut avoir une plage de sélection que si vous avez spécifié le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) quand vous l’avez créé.</span><span class="sxs-lookup"><span data-stu-id="57597-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="57597-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57597-116">Requirements</span></span>



| <span data-ttu-id="57597-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57597-117">Requirement</span></span> | <span data-ttu-id="57597-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="57597-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57597-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57597-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57597-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57597-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57597-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57597-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57597-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57597-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57597-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="57597-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57597-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57597-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57597-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57597-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="57597-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="57597-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57597-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="57597-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="57597-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="57597-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="57597-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="57597-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





