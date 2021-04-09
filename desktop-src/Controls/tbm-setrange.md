---
title: Message TBM_SETRANGE (commctrl. h)
description: Définit la plage de positions logiques minimale et maximale pour le curseur dans un TrackBar.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032611"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="753cd-104">\_Message TBM SEtrange</span><span class="sxs-lookup"><span data-stu-id="753cd-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="753cd-105">Définit la plage de positions logiques minimale et maximale pour le curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="753cd-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="753cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="753cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="753cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="753cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="753cd-108">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="753cd-108">Redraw flag.</span></span> <span data-ttu-id="753cd-109">Si ce paramètre a la **valeur true**, le TrackBar est redessiné après la définition de la plage.</span><span class="sxs-lookup"><span data-stu-id="753cd-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="753cd-110">Si ce paramètre a la **valeur false**, le message définit la plage mais ne redessine pas le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="753cd-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="753cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="753cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="753cd-112">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la position minimale du curseur, tandis que le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position maximale.</span><span class="sxs-lookup"><span data-stu-id="753cd-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="753cd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="753cd-113">Return value</span></span>

<span data-ttu-id="753cd-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="753cd-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="753cd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="753cd-115">Remarks</span></span>

<span data-ttu-id="753cd-116">Si la position actuelle du curseur est en dehors de la nouvelle plage, le message **TBM \_ SetRange** définit la position du curseur sur la nouvelle valeur maximale ou minimale.</span><span class="sxs-lookup"><span data-stu-id="753cd-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="753cd-117">Étant donné que ce message prend des valeurs entières non signées 2 16 bits, la plage maximale que ce message peut spécifier est comprise entre 0 et 65 535.</span><span class="sxs-lookup"><span data-stu-id="753cd-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="753cd-118">Pour spécifier des valeurs de plage plus grandes, utilisez les messages [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) et [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) .</span><span class="sxs-lookup"><span data-stu-id="753cd-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="753cd-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="753cd-119">Requirements</span></span>



| <span data-ttu-id="753cd-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="753cd-120">Requirement</span></span> | <span data-ttu-id="753cd-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="753cd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="753cd-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="753cd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="753cd-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="753cd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="753cd-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="753cd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="753cd-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="753cd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="753cd-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="753cd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="753cd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="753cd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="753cd-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="753cd-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="753cd-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="753cd-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="753cd-130">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="753cd-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="753cd-131">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="753cd-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

