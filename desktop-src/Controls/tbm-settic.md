---
title: Message TBM_SETTIC (commctrl. h)
description: Définit une graduation dans un TrackBar à la position logique spécifiée.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- TBM_SETTIC les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103221"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="0d60e-104">\_Message TBM SETTIC</span><span class="sxs-lookup"><span data-stu-id="0d60e-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="0d60e-105">Définit une graduation dans un TrackBar à la position logique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0d60e-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d60e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d60e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d60e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d60e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d60e-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0d60e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d60e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d60e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d60e-110">Position de la graduation.</span><span class="sxs-lookup"><span data-stu-id="0d60e-110">Position of the tick mark.</span></span> <span data-ttu-id="0d60e-111">Ce paramètre peut être n’importe laquelle des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position maximale du curseur.</span><span class="sxs-lookup"><span data-stu-id="0d60e-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d60e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d60e-112">Return value</span></span>

<span data-ttu-id="0d60e-113">Retourne la **valeur true** si la graduation est définie, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0d60e-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d60e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0d60e-114">Remarks</span></span>

<span data-ttu-id="0d60e-115">Un TrackBar crée ses propres première et dernière graduations.</span><span class="sxs-lookup"><span data-stu-id="0d60e-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="0d60e-116">N’utilisez pas ce message pour définir les première et dernière graduations.</span><span class="sxs-lookup"><span data-stu-id="0d60e-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d60e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d60e-117">Requirements</span></span>



| <span data-ttu-id="0d60e-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d60e-118">Requirement</span></span> | <span data-ttu-id="0d60e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d60e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d60e-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d60e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d60e-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d60e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d60e-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d60e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d60e-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d60e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d60e-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d60e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d60e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d60e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d60e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d60e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d60e-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0d60e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0d60e-128">**TBM \_ GETPTICS**</span><span class="sxs-lookup"><span data-stu-id="0d60e-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="0d60e-129">**TBM \_ GETTIC**</span><span class="sxs-lookup"><span data-stu-id="0d60e-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





