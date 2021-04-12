---
title: Message HDM_CLEARFILTER (commctrl. h)
description: Efface le filtre pour un contrôle d’en-tête donné. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ ClearFilter.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104491"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="1cf35-105">\_Message HDM CLEARFILTER</span><span class="sxs-lookup"><span data-stu-id="1cf35-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="1cf35-106">Efface le filtre pour un contrôle d’en-tête donné.</span><span class="sxs-lookup"><span data-stu-id="1cf35-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="1cf35-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .</span><span class="sxs-lookup"><span data-stu-id="1cf35-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cf35-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cf35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf35-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cf35-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf35-110">Valeur de colonne indiquant le filtre à effacer.</span><span class="sxs-lookup"><span data-stu-id="1cf35-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="1cf35-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cf35-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1cf35-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1cf35-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cf35-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cf35-113">Return value</span></span>

<span data-ttu-id="1cf35-114">Retourne un entier.</span><span class="sxs-lookup"><span data-stu-id="1cf35-114">Returns an integer.</span></span> <span data-ttu-id="1cf35-115">La propriété **LRESULT** est castée en un entier qui indique **true**(1) ou **false**(0).</span><span class="sxs-lookup"><span data-stu-id="1cf35-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="1cf35-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1cf35-116">Remarks</span></span>

<span data-ttu-id="1cf35-117">Si la valeur de colonne est définie sur-1, tous les filtres sont effacés et la notification [ \_ FILTERCHANGE HDN](hdn-filterchange.md) n’est envoyée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="1cf35-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf35-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cf35-118">Requirements</span></span>



| <span data-ttu-id="1cf35-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cf35-119">Requirement</span></span> | <span data-ttu-id="1cf35-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cf35-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf35-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf35-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf35-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cf35-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cf35-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cf35-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf35-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cf35-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cf35-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cf35-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cf35-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf35-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf35-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cf35-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf35-128">**ClearAllFilters d’en-tête \_**</span><span class="sxs-lookup"><span data-stu-id="1cf35-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





