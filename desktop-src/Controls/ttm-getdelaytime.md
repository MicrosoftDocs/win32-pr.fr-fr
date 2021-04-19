---
title: Message TTM_GETDELAYTIME (commctrl. h)
description: Récupère les durées initiales, contextuelles et de réaffichages actuellement définies pour un contrôle ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511565"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="71e34-104">\_Message atténuation GETDELAYTIME</span><span class="sxs-lookup"><span data-stu-id="71e34-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="71e34-105">Récupère les durées initiales, contextuelles et de réaffichages actuellement définies pour un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="71e34-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="71e34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71e34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71e34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71e34-108">Indicateur qui spécifie la valeur de durée qui sera extraite.</span><span class="sxs-lookup"><span data-stu-id="71e34-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="71e34-109">Ce paramètre peut prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="71e34-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="71e34-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="71e34-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="71e34-111">Signification</span><span class="sxs-lookup"><span data-stu-id="71e34-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="71e34-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="71e34-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="71e34-113">Récupérez la durée pendant laquelle la fenêtre d’info-bulle reste visible si le pointeur est immobile dans le rectangle englobant d’un outil.</span><span class="sxs-lookup"><span data-stu-id="71e34-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="71e34-114"><dt>**TTDT \_ initial**</dt></span><span class="sxs-lookup"><span data-stu-id="71e34-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="71e34-115">Récupérez la durée pendant laquelle le pointeur doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="71e34-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="71e34-116"><dt>**TTDT \_ RÉafficher**</dt></span><span class="sxs-lookup"><span data-stu-id="71e34-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="71e34-117">Récupérez le temps nécessaire pour que les fenêtres d’info-bulle suivantes s’affichent lorsque le pointeur se déplace d’un outil à un autre.</span><span class="sxs-lookup"><span data-stu-id="71e34-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="71e34-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71e34-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="71e34-119">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="71e34-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e34-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71e34-120">Return value</span></span>

<span data-ttu-id="71e34-121">Retourne une valeur de type INT avec la durée spécifiée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="71e34-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e34-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71e34-122">Requirements</span></span>



| <span data-ttu-id="71e34-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71e34-123">Requirement</span></span> | <span data-ttu-id="71e34-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="71e34-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71e34-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71e34-125">Minimum supported client</span></span><br/> | <span data-ttu-id="71e34-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71e34-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71e34-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71e34-127">Minimum supported server</span></span><br/> | <span data-ttu-id="71e34-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71e34-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71e34-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="71e34-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e34-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e34-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e34-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71e34-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e34-132">**ATTÉNUATION \_ SETDELAYTIME**</span><span class="sxs-lookup"><span data-stu-id="71e34-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





