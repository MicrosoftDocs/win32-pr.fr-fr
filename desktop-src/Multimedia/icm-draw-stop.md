---
title: Message ICM_DRAW_STOP (VFW. h)
description: Le message d’arrêt de l’ICM de dessin \_ \_ indique à un pilote de rendu d’arrêter son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- Message ICM_DRAW_STOP Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464994"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="7028e-105">Message d’arrêt du \_ dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="7028e-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="7028e-106">Le message d' **\_ \_ arrêt** de l’ICM de dessin indique à un pilote de rendu d’arrêter son horloge interne pour le minutage des frames de dessin.</span><span class="sxs-lookup"><span data-stu-id="7028e-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="7028e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .</span><span class="sxs-lookup"><span data-stu-id="7028e-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="7028e-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7028e-108">Return Value</span></span>

<span data-ttu-id="7028e-109">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7028e-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7028e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7028e-110">Remarks</span></span>

<span data-ttu-id="7028e-111">Ce message est utilisé par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.</span><span class="sxs-lookup"><span data-stu-id="7028e-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7028e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7028e-112">Requirements</span></span>



| <span data-ttu-id="7028e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7028e-113">Requirement</span></span> | <span data-ttu-id="7028e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7028e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7028e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7028e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7028e-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7028e-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7028e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7028e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7028e-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7028e-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7028e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7028e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7028e-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7028e-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7028e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7028e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7028e-122">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="7028e-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7028e-123">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="7028e-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





