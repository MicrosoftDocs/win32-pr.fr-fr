---
title: Message MCM_GETMAXSELCOUNT (commctrl. h)
description: Récupère la plage de dates maximale pouvant être sélectionnée dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- MCM_GETMAXSELCOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033014"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="437c4-105">\_Message GETMAXSELCOUNT MCM</span><span class="sxs-lookup"><span data-stu-id="437c4-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="437c4-106">Récupère la plage de dates maximale pouvant être sélectionnée dans un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="437c4-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="437c4-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="437c4-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="437c4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="437c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="437c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="437c4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="437c4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="437c4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="437c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="437c4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="437c4-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="437c4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="437c4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="437c4-113">Return value</span></span>

<span data-ttu-id="437c4-114">Retourne une valeur INT qui représente le nombre total de jours pouvant être sélectionnés pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="437c4-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="437c4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="437c4-115">Remarks</span></span>

<span data-ttu-id="437c4-116">Vous pouvez modifier la plage de dates maximale pouvant être sélectionnée à l’aide du message [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="437c4-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="437c4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="437c4-117">Requirements</span></span>



| <span data-ttu-id="437c4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="437c4-118">Requirement</span></span> | <span data-ttu-id="437c4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="437c4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="437c4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="437c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="437c4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="437c4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="437c4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="437c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="437c4-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="437c4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="437c4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="437c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="437c4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="437c4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





