---
title: Message ICM_GETBUFFERSWANTED (VFW. h)
description: Le \_ message GETBUFFERSWANTED ICM interroge un pilote sur le nombre de mémoires tampons à allouer. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- Message ICM_GETBUFFERSWANTED Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941789"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="c85ca-105">\_Message GETBUFFERSWANTED ICM</span><span class="sxs-lookup"><span data-stu-id="c85ca-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="c85ca-106">Le **message \_ GETBUFFERSWANTED ICM** interroge un pilote sur le nombre de mémoires tampons à allouer.</span><span class="sxs-lookup"><span data-stu-id="c85ca-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="c85ca-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .</span><span class="sxs-lookup"><span data-stu-id="c85ca-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="c85ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c85ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c85ca-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span><span class="sxs-lookup"><span data-stu-id="c85ca-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="c85ca-110">Adresse qui contient le nombre d’échantillons dont le pilote a besoin pour restituer efficacement les données.</span><span class="sxs-lookup"><span data-stu-id="c85ca-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c85ca-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c85ca-111">Return Value</span></span>

<span data-ttu-id="c85ca-112">Retourne ICERR \_ OK en cas de réussite ou ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c85ca-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c85ca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c85ca-113">Remarks</span></span>

<span data-ttu-id="c85ca-114">Ce message est utilisé par les pilotes qui utilisent le matériel pour afficher les données et qui souhaitent garantir un délai minimal en raison de l’arrivée d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c85ca-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="c85ca-115">Par exemple, si un pilote contrôle une carte de décompression vidéo qui peut contenir 10 images vidéo, il peut renvoyer 10 pour ce message.</span><span class="sxs-lookup"><span data-stu-id="c85ca-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="c85ca-116">Cela indique aux applications d’essayer de conserver 10 frames à l’avance du frame dont il a besoin.</span><span class="sxs-lookup"><span data-stu-id="c85ca-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="c85ca-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c85ca-117">Requirements</span></span>



| <span data-ttu-id="c85ca-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c85ca-118">Requirement</span></span> | <span data-ttu-id="c85ca-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c85ca-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c85ca-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c85ca-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c85ca-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c85ca-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c85ca-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c85ca-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c85ca-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c85ca-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c85ca-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c85ca-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c85ca-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c85ca-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c85ca-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c85ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85ca-127">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="c85ca-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c85ca-128">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="c85ca-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





