---
title: Message TBM_SETTIPSIDE (commctrl. h)
description: Positionne un contrôle ToolTip utilisé par un contrôle TrackBar. Les contrôles TrackBar qui utilisent le \_ style des info-bulles tbs affichent des info-bulles.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384263"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="bb710-105">\_Message TBM SETTIPSIDE</span><span class="sxs-lookup"><span data-stu-id="bb710-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="bb710-106">Positionne un contrôle ToolTip utilisé par un contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bb710-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="bb710-107">Les contrôles TrackBar qui utilisent le style des [**\_ info-bulles tbs**](trackbar-control-styles.md) affichent des info-bulles.</span><span class="sxs-lookup"><span data-stu-id="bb710-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb710-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb710-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb710-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb710-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb710-110">Valeur représentant l’emplacement d’affichage du contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="bb710-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="bb710-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb710-111">This value can be one of the following:</span></span>



| <span data-ttu-id="bb710-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb710-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="bb710-113">Signification</span><span class="sxs-lookup"><span data-stu-id="bb710-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="bb710-114"><dt>**TBTS \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="bb710-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="bb710-115">Le contrôle ToolTip est positionné au-dessus du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bb710-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="bb710-116">Cet indicateur est destiné à être utilisé avec le trackbars horizontal.</span><span class="sxs-lookup"><span data-stu-id="bb710-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="bb710-117"><dt>**TBTS \_ gauche**</dt></span><span class="sxs-lookup"><span data-stu-id="bb710-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="bb710-118">Le contrôle ToolTip sera positionné à gauche du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bb710-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="bb710-119">Cet indicateur est destiné à être utilisé avec le trackbars vertical.</span><span class="sxs-lookup"><span data-stu-id="bb710-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="bb710-120"><dt>**TBTS \_ bas**</dt></span><span class="sxs-lookup"><span data-stu-id="bb710-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="bb710-121">Le contrôle ToolTip sera positionné sous le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bb710-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="bb710-122">Cet indicateur est destiné à être utilisé avec le trackbars horizontal.</span><span class="sxs-lookup"><span data-stu-id="bb710-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="bb710-123"><dt>**TBTS \_ droit**</dt></span><span class="sxs-lookup"><span data-stu-id="bb710-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="bb710-124">Le contrôle ToolTip est positionné à droite du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="bb710-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="bb710-125">Cet indicateur est destiné à être utilisé avec le trackbars vertical.</span><span class="sxs-lookup"><span data-stu-id="bb710-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bb710-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb710-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bb710-127">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="bb710-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb710-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb710-128">Return value</span></span>

<span data-ttu-id="bb710-129">Retourne une valeur qui représente l’emplacement précédent du contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="bb710-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="bb710-130">La valeur de retour est égale à l’une des valeurs possibles pour *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bb710-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb710-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb710-131">Requirements</span></span>



| <span data-ttu-id="bb710-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb710-132">Requirement</span></span> | <span data-ttu-id="bb710-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb710-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb710-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb710-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bb710-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb710-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb710-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb710-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bb710-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb710-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb710-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb710-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb710-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb710-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





