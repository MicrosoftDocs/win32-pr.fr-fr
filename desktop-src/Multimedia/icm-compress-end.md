---
title: Message ICM_COMPRESS_END (VFW. h)
description: Le message de fin de compression ICM \_ \_ indique à un pilote de compression vidéo d’arrêter la compression et les ressources gratuites allouées pour la compression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- Message ICM_COMPRESS_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464835"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="58b5a-105">Message de fin de \_ compression ICM \_</span><span class="sxs-lookup"><span data-stu-id="58b5a-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="58b5a-106">Le message de **\_ \_ fin** de compression ICM indique à un pilote de compression vidéo d’arrêter la compression et les ressources gratuites allouées pour la compression.</span><span class="sxs-lookup"><span data-stu-id="58b5a-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="58b5a-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .</span><span class="sxs-lookup"><span data-stu-id="58b5a-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="58b5a-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58b5a-108">Return Value</span></span>

<span data-ttu-id="58b5a-109">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="58b5a-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b5a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="58b5a-110">Remarks</span></span>

<span data-ttu-id="58b5a-111">VCM enregistre les paramètres du message de début de la [**\_ \_ compression ICM**](icm-compress-begin.md) le plus récent.</span><span class="sxs-lookup"><span data-stu-id="58b5a-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="58b5a-112">**ICM \_ Les \_** **\_ \_ terminaisons** de compression Begin et ICM ne sont pas imbriquées.</span><span class="sxs-lookup"><span data-stu-id="58b5a-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="58b5a-113">Si votre pilote reçoit la compression ICM avant que la compression soit arrêtée avec la **\_ \_ terminaison** de compression ICM, il doit redémarrer la compression avec les nouveaux paramètres. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="58b5a-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="58b5a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58b5a-114">Requirements</span></span>



| <span data-ttu-id="58b5a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58b5a-115">Requirement</span></span> | <span data-ttu-id="58b5a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="58b5a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="58b5a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58b5a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="58b5a-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58b5a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="58b5a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58b5a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="58b5a-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58b5a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58b5a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="58b5a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="58b5a-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="58b5a-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58b5a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58b5a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b5a-124">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="58b5a-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="58b5a-125">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="58b5a-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





