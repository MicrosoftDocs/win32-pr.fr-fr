---
description: Déclenché par une sortie approuvée si une erreur se produit lors de l’application de la stratégie de sortie.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Événement MEPolicyError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518603"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="294c0-103">Événement MEPolicyError</span><span class="sxs-lookup"><span data-stu-id="294c0-103">MEPolicyError event</span></span>

<span data-ttu-id="294c0-104">Déclenché par une sortie approuvée si une erreur se produit lors de l’application de la stratégie de sortie.</span><span class="sxs-lookup"><span data-stu-id="294c0-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="294c0-105">Si la session multimédia reçoit cet événement, elle arrête la lecture et transfère l’événement à l’application.</span><span class="sxs-lookup"><span data-stu-id="294c0-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="294c0-106">Valeurs d’événement</span><span class="sxs-lookup"><span data-stu-id="294c0-106">Event values</span></span>

<span data-ttu-id="294c0-107">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="294c0-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="294c0-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="294c0-108">VARTYPE</span></span>              | <span data-ttu-id="294c0-109">Description</span><span class="sxs-lookup"><span data-stu-id="294c0-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="294c0-110">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="294c0-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="294c0-111">Aucune donnée d'événement.</span><span class="sxs-lookup"><span data-stu-id="294c0-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="294c0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="294c0-112">Remarks</span></span>

<span data-ttu-id="294c0-113">Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="294c0-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="294c0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="294c0-114">Value</span></span>                      | <span data-ttu-id="294c0-115">Description</span><span class="sxs-lookup"><span data-stu-id="294c0-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="294c0-116">\_stratégie MF \_ E \_ non prise en charge</span><span class="sxs-lookup"><span data-stu-id="294c0-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="294c0-117">La sortie approuvée ne prend pas en charge la stratégie de sortie actuelle.</span><span class="sxs-lookup"><span data-stu-id="294c0-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="294c0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="294c0-118">Requirements</span></span>



| <span data-ttu-id="294c0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="294c0-119">Requirement</span></span> | <span data-ttu-id="294c0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="294c0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="294c0-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="294c0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="294c0-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="294c0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="294c0-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="294c0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="294c0-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="294c0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="294c0-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="294c0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="294c0-126"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="294c0-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="294c0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="294c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="294c0-128">Événements de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="294c0-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




