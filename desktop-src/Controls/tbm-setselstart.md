---
title: Message TBM_SETSELSTART (commctrl. h)
description: Définit la position logique de départ de la plage de sélection actuelle dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le \_ style tbs ENABLESELRANGE.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032339"
---
# <a name="tbm_setselstart-message"></a><span data-ttu-id="a73ee-105">\_Message TBM SETSELSTART</span><span class="sxs-lookup"><span data-stu-id="a73ee-105">TBM\_SETSELSTART message</span></span>

<span data-ttu-id="a73ee-106">Définit la position logique de départ de la plage de sélection actuelle dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a73ee-106">Sets the starting logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="a73ee-107">Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a73ee-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a73ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a73ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a73ee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a73ee-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a73ee-110">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="a73ee-110">Redraw flag.</span></span> <span data-ttu-id="a73ee-111">Si ce paramètre a la **valeur true**, le message redessine le TrackBar une fois la plage de sélection définie.</span><span class="sxs-lookup"><span data-stu-id="a73ee-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="a73ee-112">Si ce paramètre a la **valeur false**, le message définit la plage de sélection, mais ne redessine pas le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="a73ee-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="a73ee-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a73ee-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a73ee-114">Position de départ de la plage de sélection.</span><span class="sxs-lookup"><span data-stu-id="a73ee-114">Starting position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a73ee-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a73ee-115">Return value</span></span>

<span data-ttu-id="a73ee-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a73ee-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73ee-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a73ee-117">Requirements</span></span>



| <span data-ttu-id="a73ee-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a73ee-118">Requirement</span></span> | <span data-ttu-id="a73ee-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a73ee-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a73ee-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73ee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a73ee-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a73ee-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a73ee-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a73ee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a73ee-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a73ee-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a73ee-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a73ee-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a73ee-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73ee-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73ee-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a73ee-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a73ee-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a73ee-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a73ee-128">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="a73ee-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="a73ee-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="a73ee-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="a73ee-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="a73ee-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="a73ee-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="a73ee-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> </dl>

 

 





