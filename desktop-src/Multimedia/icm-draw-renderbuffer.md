---
title: Message ICM_DRAW_RENDERBUFFER (VFW. h)
description: Le \_ message RENDERBUFFER de dessin ICM \_ indique à un pilote de rendu de dessiner les frames qui lui ont été transmis. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- Message ICM_DRAW_RENDERBUFFER Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942595"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="378c8-105">\_Message RENDERBUFFER de dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="378c8-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="378c8-106">Le **message \_ \_ RENDERBUFFER de dessin ICM** indique à un pilote de rendu de dessiner les frames qui lui ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="378c8-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="378c8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .</span><span class="sxs-lookup"><span data-stu-id="378c8-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="378c8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="378c8-108">Return Value</span></span>

<span data-ttu-id="378c8-109">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="378c8-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="378c8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="378c8-110">Remarks</span></span>

<span data-ttu-id="378c8-111">Utilisez ce message avec un matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.</span><span class="sxs-lookup"><span data-stu-id="378c8-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="378c8-112">Ce message est généralement utilisé pour effectuer une opération de recherche lorsque le pilote doit être spécifiquement invité à afficher chaque image vidéo qui lui est transmise au lieu de lancer une séquence de trames vidéo.</span><span class="sxs-lookup"><span data-stu-id="378c8-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="378c8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="378c8-113">Requirements</span></span>



| <span data-ttu-id="378c8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="378c8-114">Requirement</span></span> | <span data-ttu-id="378c8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="378c8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="378c8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="378c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="378c8-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="378c8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="378c8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="378c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="378c8-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="378c8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="378c8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="378c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="378c8-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="378c8-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="378c8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="378c8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378c8-123">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="378c8-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="378c8-124">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="378c8-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





