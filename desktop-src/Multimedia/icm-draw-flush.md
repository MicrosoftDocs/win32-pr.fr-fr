---
title: Message ICM_DRAW_FLUSH (VFW. h)
description: Le \_ \_ message de vidage de dessin ICM indique à un pilote de rendu de restituer le contenu de toutes les mémoires tampons d’image qui sont en attente de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- Message ICM_DRAW_FLUSH Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513791"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="c2183-105">Message de vidage de \_ dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="c2183-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="c2183-106">Le message de **\_ \_ vidage de dessin ICM** indique à un pilote de rendu de restituer le contenu de toutes les mémoires tampons d’image qui sont en attente de dessin.</span><span class="sxs-lookup"><span data-stu-id="c2183-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="c2183-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .</span><span class="sxs-lookup"><span data-stu-id="c2183-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c2183-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c2183-108">Return Value</span></span>

<span data-ttu-id="c2183-109">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2183-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2183-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c2183-110">Remarks</span></span>

<span data-ttu-id="c2183-111">Ce message est utilisé uniquement par le matériel qui effectue sa propre décompression asynchrone, son minutage et son dessin.</span><span class="sxs-lookup"><span data-stu-id="c2183-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2183-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2183-112">Requirements</span></span>



| <span data-ttu-id="c2183-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2183-113">Requirement</span></span> | <span data-ttu-id="c2183-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2183-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c2183-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2183-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2183-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2183-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c2183-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2183-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2183-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2183-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2183-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2183-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2183-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2183-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2183-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2183-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2183-122">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="c2183-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c2183-123">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="c2183-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





