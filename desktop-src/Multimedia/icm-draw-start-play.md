---
title: Message ICM_DRAW_START_PLAY (VFW. h)
description: Le \_ \_ \_ message de début de dessin ICM fournit les heures de début et de fin d’une opération de lecture à un pilote de rendu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- Message ICM_DRAW_START_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103449"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="f1ff8-105">Message de début de la \_ \_ \_ lecture ICM</span><span class="sxs-lookup"><span data-stu-id="f1ff8-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="f1ff8-106">Le message de **début de dessin ICM fournit les \_ \_ \_** heures de début et de fin d’une opération de lecture à un pilote de rendu.</span><span class="sxs-lookup"><span data-stu-id="f1ff8-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="f1ff8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .</span><span class="sxs-lookup"><span data-stu-id="f1ff8-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="f1ff8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1ff8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ff8-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span><span class="sxs-lookup"><span data-stu-id="f1ff8-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="f1ff8-110">Heure de début</span><span class="sxs-lookup"><span data-stu-id="f1ff8-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="f1ff8-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*Supports*</span><span class="sxs-lookup"><span data-stu-id="f1ff8-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="f1ff8-112">Heure de fin.</span><span class="sxs-lookup"><span data-stu-id="f1ff8-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ff8-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1ff8-113">Return Value</span></span>

<span data-ttu-id="f1ff8-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f1ff8-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ff8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f1ff8-115">Remarks</span></span>

<span data-ttu-id="f1ff8-116">Ce message précède toutes les données de frame envoyées au pilote de rendu.</span><span class="sxs-lookup"><span data-stu-id="f1ff8-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="f1ff8-117">Les unités pour *lFrom* et *lTo* sont spécifiées avec le message [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ff8-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="f1ff8-118">Pour les données vidéo, il s’agit généralement d’un nombre de trames.</span><span class="sxs-lookup"><span data-stu-id="f1ff8-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="f1ff8-119">Pour plus d’informations sur la vitesse de lecture, consultez les membres **dwRate** et **dwScale** de la structure [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .</span><span class="sxs-lookup"><span data-stu-id="f1ff8-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="f1ff8-120">Si l’heure de fin est inférieure à l’heure de début, la direction de la lecture est inversée.</span><span class="sxs-lookup"><span data-stu-id="f1ff8-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ff8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1ff8-121">Requirements</span></span>



| <span data-ttu-id="f1ff8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1ff8-122">Requirement</span></span> | <span data-ttu-id="f1ff8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1ff8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1ff8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ff8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1ff8-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1ff8-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1ff8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1ff8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1ff8-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1ff8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1ff8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1ff8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1ff8-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1ff8-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ff8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1ff8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ff8-131">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="f1ff8-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f1ff8-132">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="f1ff8-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





