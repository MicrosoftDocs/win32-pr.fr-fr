---
title: Message TBM_GETCHANNELRECT (commctrl. h)
description: Récupère la taille et la position du rectangle englobant pour le canal d’un TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- TBM_GETCHANNELRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941842"
---
# <a name="tbm_getchannelrect-message"></a><span data-ttu-id="b3a52-104">\_Message TBM GETCHANNELRECT</span><span class="sxs-lookup"><span data-stu-id="b3a52-104">TBM\_GETCHANNELRECT message</span></span>

<span data-ttu-id="b3a52-105">Récupère la taille et la position du rectangle englobant pour le canal d’un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b3a52-105">Retrieves the size and position of the bounding rectangle for a trackbar's channel.</span></span> <span data-ttu-id="b3a52-106">(Le canal est la zone sur laquelle le curseur se déplace.</span><span class="sxs-lookup"><span data-stu-id="b3a52-106">(The channel is the area over which the slider moves.</span></span> <span data-ttu-id="b3a52-107">Elle contient la surbrillance lorsqu’une plage est sélectionnée.)</span><span class="sxs-lookup"><span data-stu-id="b3a52-107">It contains the highlight when a range is selected.)</span></span>

## <a name="parameters"></a><span data-ttu-id="b3a52-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3a52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a52-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3a52-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3a52-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b3a52-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3a52-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3a52-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a52-112">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b3a52-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="b3a52-113">Le message remplit cette structure à l’aide du rectangle englobant du canal, dans les coordonnées clientes de la fenêtre du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b3a52-113">The message fills this structure with the channel's bounding rectangle, in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a52-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3a52-114">Return value</span></span>

<span data-ttu-id="b3a52-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b3a52-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a52-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3a52-116">Requirements</span></span>



| <span data-ttu-id="b3a52-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3a52-117">Requirement</span></span> | <span data-ttu-id="b3a52-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3a52-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a52-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3a52-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a52-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3a52-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3a52-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3a52-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a52-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3a52-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3a52-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3a52-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3a52-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a52-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

