---
title: Message PBM_SETRANGE (commctrl. h)
description: Définit les valeurs minimale et maximale d’une barre de progression et redessine la barre pour refléter la nouvelle plage.
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843929"
---
# <a name="pbm_setrange-message"></a><span data-ttu-id="f0f90-104">\_Message PBM</span><span class="sxs-lookup"><span data-stu-id="f0f90-104">PBM\_SETRANGE message</span></span>

<span data-ttu-id="f0f90-105">Définit les valeurs minimale et maximale d’une barre de progression et redessine la barre pour refléter la nouvelle plage.</span><span class="sxs-lookup"><span data-stu-id="f0f90-105">Sets the minimum and maximum values for a progress bar and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0f90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0f90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0f90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0f90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0f90-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f0f90-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0f90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0f90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0f90-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la valeur de plage minimale et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la valeur de plage maximale.</span><span class="sxs-lookup"><span data-stu-id="f0f90-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum range value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum range value.</span></span> <span data-ttu-id="f0f90-111">La valeur de plage minimale ne doit pas être négative.</span><span class="sxs-lookup"><span data-stu-id="f0f90-111">The minimum range value must not be negative.</span></span> <span data-ttu-id="f0f90-112">Par défaut, la valeur minimale est zéro.</span><span class="sxs-lookup"><span data-stu-id="f0f90-112">By default, the minimum value is zero.</span></span> <span data-ttu-id="f0f90-113">La valeur de plage maximale doit être supérieure à la valeur de plage minimale.</span><span class="sxs-lookup"><span data-stu-id="f0f90-113">The maximum range value must be greater than the minimum range value.</span></span> <span data-ttu-id="f0f90-114">Par défaut, la valeur de plage maximale est 100.</span><span class="sxs-lookup"><span data-stu-id="f0f90-114">By default, the maximum range value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0f90-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0f90-115">Return value</span></span>

<span data-ttu-id="f0f90-116">Retourne les valeurs de la plage précédente en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f0f90-116">Returns the previous range values if successful, or zero otherwise.</span></span> <span data-ttu-id="f0f90-117">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la valeur minimale précédente et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la valeur maximale précédente.</span><span class="sxs-lookup"><span data-stu-id="f0f90-117">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the previous minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the previous maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0f90-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f0f90-118">Remarks</span></span>

<span data-ttu-id="f0f90-119">Si vous ne définissez pas les valeurs de plage, le système définit la valeur minimale sur 0 et la valeur maximale sur 100.</span><span class="sxs-lookup"><span data-stu-id="f0f90-119">If you do not set the range values, the system sets the minimum value to 0 and the maximum value to 100.</span></span> <span data-ttu-id="f0f90-120">Étant donné que ce message exprime la plage en tant qu’entier non signé 16 bits, il peut s’étendre de 0 à 65 535.</span><span class="sxs-lookup"><span data-stu-id="f0f90-120">Because this message expresses the range as a 16-bit unsigned integer, it can extend from 0 to 65,535.</span></span> <span data-ttu-id="f0f90-121">La valeur minimale de la plage peut être comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="f0f90-121">The minimum value in the range can be from 0 to 65,535.</span></span> <span data-ttu-id="f0f90-122">De même, la valeur maximale peut être comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="f0f90-122">Likewise, the maximum value can be from 0 to 65,535.</span></span>

<span data-ttu-id="f0f90-123">Pour définir une plage plus grande, appelez [**PBM \_ SETRANGE32**](pbm-setrange32.md).</span><span class="sxs-lookup"><span data-stu-id="f0f90-123">To set a larger range, call [**PBM\_SETRANGE32**](pbm-setrange32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f90-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0f90-124">Requirements</span></span>



| <span data-ttu-id="f0f90-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0f90-125">Requirement</span></span> | <span data-ttu-id="f0f90-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0f90-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f90-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0f90-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f0f90-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0f90-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0f90-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0f90-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f0f90-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0f90-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0f90-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0f90-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0f90-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0f90-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0f90-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0f90-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f0f90-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f0f90-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f0f90-135">**\_GETRANGE PBM**</span><span class="sxs-lookup"><span data-stu-id="f0f90-135">**PBM\_GETRANGE**</span></span>](pbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="f0f90-136">**\_SETRANGE32 PBM**</span><span class="sxs-lookup"><span data-stu-id="f0f90-136">**PBM\_SETRANGE32**</span></span>](pbm-setrange32.md)
</dt> </dl>

 

