---
title: Message ICM_DRAW_STOP_PLAY (VFW. h)
description: Le \_ message ICM Draw \_ Stop \_ Play avertit un pilote de rendu quand une opération de lecture est terminée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- Message ICM_DRAW_STOP_PLAY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106552"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="ef7a5-105">Message d’arrêt de la \_ \_ \_ lecture ICM</span><span class="sxs-lookup"><span data-stu-id="ef7a5-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="ef7a5-106">Le message **ICM \_ Draw \_ Stop \_ Play** avertit un pilote de rendu quand une opération de lecture est terminée.</span><span class="sxs-lookup"><span data-stu-id="ef7a5-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="ef7a5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .</span><span class="sxs-lookup"><span data-stu-id="ef7a5-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ef7a5-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef7a5-108">Return Value</span></span>

<span data-ttu-id="ef7a5-109">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ef7a5-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef7a5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="ef7a5-110">Remarks</span></span>

<span data-ttu-id="ef7a5-111">Utilisez ce message lorsque l’opération de lecture est terminée.</span><span class="sxs-lookup"><span data-stu-id="ef7a5-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="ef7a5-112">Utilisez le message [**ICM \_ Draw \_ Stop**](icm-draw-stop.md) pour terminer le minutage.</span><span class="sxs-lookup"><span data-stu-id="ef7a5-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef7a5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef7a5-113">Requirements</span></span>



| <span data-ttu-id="ef7a5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef7a5-114">Requirement</span></span> | <span data-ttu-id="ef7a5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef7a5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef7a5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef7a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef7a5-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef7a5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ef7a5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef7a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef7a5-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef7a5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef7a5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef7a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef7a5-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef7a5-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef7a5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef7a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef7a5-123">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ef7a5-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ef7a5-124">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ef7a5-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





