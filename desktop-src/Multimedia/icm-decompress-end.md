---
title: Message ICM_DECOMPRESS_END (VFW. h)
description: Le message de fin de décompression ICM \_ \_ indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- Message ICM_DECOMPRESS_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742972"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="6e8d1-105">\_Message de fin de décompression ICM \_</span><span class="sxs-lookup"><span data-stu-id="6e8d1-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="6e8d1-106">Le message de **\_ \_ fin** de décompression ICM indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression.</span><span class="sxs-lookup"><span data-stu-id="6e8d1-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="6e8d1-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="6e8d1-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="6e8d1-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e8d1-108">Return Value</span></span>

<span data-ttu-id="6e8d1-109">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6e8d1-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e8d1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6e8d1-110">Remarks</span></span>

<span data-ttu-id="6e8d1-111">Le pilote doit libérer toutes les ressources allouées pour le message de début de la [**\_ \_ décompression ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="6e8d1-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="6e8d1-112">[**ICM \_ \_**](icm-decompress-begin.md) Les **\_ \_ terminaisons** de décompression Begin et ICM ne sont pas imbriquées.</span><span class="sxs-lookup"><span data-stu-id="6e8d1-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="6e8d1-113">Si le pilote reçoit la décompression ICM avant que la décompression ne soit arrêtée avec la **\_ \_ fin** de la décompression ICM, il doit redémarrer la décompression avec les nouveaux paramètres. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="6e8d1-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e8d1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e8d1-114">Requirements</span></span>



| <span data-ttu-id="6e8d1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e8d1-115">Requirement</span></span> | <span data-ttu-id="6e8d1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e8d1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6e8d1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e8d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e8d1-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e8d1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6e8d1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e8d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e8d1-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e8d1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e8d1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e8d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e8d1-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e8d1-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e8d1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e8d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e8d1-124">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="6e8d1-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6e8d1-125">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="6e8d1-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





