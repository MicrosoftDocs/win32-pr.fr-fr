---
title: Message UDM_SETRANGE (commctrl. h)
description: Définit les positions minimale et maximale (plage) pour un contrôle up-up.
ms.assetid: 81875528-86cc-419a-a07c-f4f98baf1462
keywords:
- UDM_SETRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb32a72ca8ca5182e87e2c0346cbc44ab25300e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033039"
---
# <a name="udm_setrange-message"></a><span data-ttu-id="a7239-104">\_Message UDM SEtrange</span><span class="sxs-lookup"><span data-stu-id="a7239-104">UDM\_SETRANGE message</span></span>

<span data-ttu-id="a7239-105">Définit les positions minimale et maximale (plage) pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="a7239-105">Sets the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7239-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7239-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7239-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7239-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a7239-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a7239-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a7239-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7239-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7239-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **short** qui spécifie la position maximale pour le contrôle up-UpDown, et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **short** qui spécifie la position minimale.</span><span class="sxs-lookup"><span data-stu-id="a7239-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **short** that specifies the maximum position for the up-down control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **short** that specifies the minimum position.</span></span> <span data-ttu-id="a7239-111">Aucune position ne peut être supérieure à la \_ valeur ud MAXVAL ou inférieure à la \_ valeur ud MINVAL.</span><span class="sxs-lookup"><span data-stu-id="a7239-111">Neither position can be greater than the UD\_MAXVAL value or less than the UD\_MINVAL value.</span></span> <span data-ttu-id="a7239-112">En outre, la différence entre les deux positions ne peut pas dépasser UD \_ MAXVAL.</span><span class="sxs-lookup"><span data-stu-id="a7239-112">In addition, the difference between the two positions cannot exceed UD\_MAXVAL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7239-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7239-113">Return value</span></span>

<span data-ttu-id="a7239-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a7239-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7239-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a7239-115">Remarks</span></span>

<span data-ttu-id="a7239-116">La position maximale peut être inférieure à la position minimale.</span><span class="sxs-lookup"><span data-stu-id="a7239-116">The maximum position can be less than the minimum position.</span></span> <span data-ttu-id="a7239-117">Le fait de cliquer sur le bouton fléché vers le haut déplace la position actuelle plus près de la position maximale, et le fait de cliquer sur le bouton fléché vers le bas se déplace vers la position minimale.</span><span class="sxs-lookup"><span data-stu-id="a7239-117">Clicking the up arrow button moves the current position closer to the maximum position, and clicking the down arrow button moves toward the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7239-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7239-118">Requirements</span></span>



| <span data-ttu-id="a7239-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7239-119">Requirement</span></span> | <span data-ttu-id="a7239-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7239-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7239-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7239-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a7239-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7239-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7239-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7239-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a7239-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7239-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7239-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7239-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7239-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7239-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7239-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7239-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7239-128">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="a7239-128">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[<span data-ttu-id="a7239-129">**e \_ trange UDM**</span><span class="sxs-lookup"><span data-stu-id="a7239-129">**UDM\_SETRANGE**</span></span>](udm-setrange.md)
</dt> </dl>

 

