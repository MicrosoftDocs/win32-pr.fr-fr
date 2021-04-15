---
title: Message TBM_CLEARTICS (commctrl. h)
description: Supprime les graduations actuelles d’un TrackBar. Ce message ne supprime pas les première et dernière graduations, qui sont créées automatiquement par le TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464778"
---
# <a name="tbm_cleartics-message"></a><span data-ttu-id="8275a-105">\_Message TBM CLEARTICS</span><span class="sxs-lookup"><span data-stu-id="8275a-105">TBM\_CLEARTICS message</span></span>

<span data-ttu-id="8275a-106">Supprime les graduations actuelles d’un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8275a-106">Removes the current tick marks from a trackbar.</span></span> <span data-ttu-id="8275a-107">Ce message ne supprime pas les première et dernière graduations, qui sont créées automatiquement par le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8275a-107">This message does not remove the first and last tick marks, which are created automatically by the trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8275a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8275a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8275a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8275a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8275a-110">Indicateur de redessin.</span><span class="sxs-lookup"><span data-stu-id="8275a-110">Redraw flag.</span></span> <span data-ttu-id="8275a-111">Si ce paramètre a la **valeur true**, le TrackBar est redessiné après l’effacement des graduations.</span><span class="sxs-lookup"><span data-stu-id="8275a-111">If this parameter is **TRUE**, the trackbar is redrawn after the tick marks are cleared.</span></span> <span data-ttu-id="8275a-112">Si ce paramètre a la **valeur false**, le message efface les graduations, mais ne redessine pas le TrackBar.</span><span class="sxs-lookup"><span data-stu-id="8275a-112">If this parameter is **FALSE**, the message clears the tick marks but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="8275a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8275a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8275a-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8275a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8275a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8275a-115">Return value</span></span>

<span data-ttu-id="8275a-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8275a-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8275a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8275a-117">Requirements</span></span>



| <span data-ttu-id="8275a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8275a-118">Requirement</span></span> | <span data-ttu-id="8275a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8275a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8275a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8275a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8275a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8275a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8275a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8275a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8275a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8275a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8275a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8275a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8275a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8275a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





