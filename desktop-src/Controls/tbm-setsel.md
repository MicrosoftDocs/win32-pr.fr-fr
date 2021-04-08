---
title: Message TBM_SETSEL (commctrl. h)
description: Définit les positions de début et de fin de la plage de sélection disponible dans un TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739901"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="4e326-104">\_Message TBM SETSEL</span><span class="sxs-lookup"><span data-stu-id="4e326-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="4e326-105">Définit les positions de début et de fin de la plage de sélection disponible dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4e326-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e326-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e326-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e326-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e326-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="4e326-108">Redraw flag.</span></span> <span data-ttu-id="4e326-109">Si ce paramètre a la **valeur true**, le message redessine le TrackBar une fois la plage de sélection définie.</span><span class="sxs-lookup"><span data-stu-id="4e326-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="4e326-110">Si ce paramètre a la **valeur false**, le message définit la plage de sélection, mais ne redessine pas le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="4e326-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="4e326-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e326-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e326-112">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la position logique de départ pour la plage de sélection, tandis que le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position logique de fin.</span><span class="sxs-lookup"><span data-stu-id="4e326-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e326-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e326-113">Return value</span></span>

<span data-ttu-id="4e326-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4e326-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e326-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4e326-115">Remarks</span></span>

<span data-ttu-id="4e326-116">Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ ENABLESELRANGE**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4e326-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="4e326-117">**TBM \_ SETSEL** vous permet de limiter le pointeur à une partie de la plage disponible pour la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="4e326-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e326-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e326-118">Requirements</span></span>



| <span data-ttu-id="4e326-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e326-119">Requirement</span></span> | <span data-ttu-id="4e326-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e326-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e326-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e326-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e326-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e326-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e326-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e326-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e326-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e326-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e326-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e326-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e326-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e326-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e326-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e326-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e326-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4e326-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e326-129">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="4e326-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="4e326-130">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="4e326-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="4e326-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="4e326-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="4e326-132">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="4e326-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

