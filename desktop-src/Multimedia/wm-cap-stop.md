---
title: Message WM_CAP_STOP (VFW. h)
description: Le \_ message WM Cap \_ Stop arrête l’opération de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- Message WM_CAP_STOP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743540"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="fce0f-105">Message d’arrêt de l' \_ embout WM \_</span><span class="sxs-lookup"><span data-stu-id="fce0f-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="fce0f-106">Le message **WM \_ Cap \_ Stop** arrête l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="fce0f-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="fce0f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .</span><span class="sxs-lookup"><span data-stu-id="fce0f-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="fce0f-108">Dans la capture de frame de l’étape, les données d’image qui ont été collectées avant l’envoi de ce message sont conservées dans le fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="fce0f-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="fce0f-109">Une durée équivalente des données audio est également conservée dans le fichier de capture si la capture audio a été activée.</span><span class="sxs-lookup"><span data-stu-id="fce0f-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="fce0f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fce0f-110">Return Value</span></span>

<span data-ttu-id="fce0f-111">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fce0f-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce0f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fce0f-112">Remarks</span></span>

<span data-ttu-id="fce0f-113">L’opération de capture doit donner l’utilisation de ce message.</span><span class="sxs-lookup"><span data-stu-id="fce0f-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="fce0f-114">Utilisez le message [**WM \_ Cap \_ Abort**](wm-cap-abort.md) pour abandonner l’opération de capture en cours.</span><span class="sxs-lookup"><span data-stu-id="fce0f-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce0f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fce0f-115">Requirements</span></span>



| <span data-ttu-id="fce0f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fce0f-116">Requirement</span></span> | <span data-ttu-id="fce0f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fce0f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fce0f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce0f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fce0f-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fce0f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fce0f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fce0f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fce0f-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fce0f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fce0f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="fce0f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce0f-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce0f-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce0f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fce0f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce0f-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="fce0f-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fce0f-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="fce0f-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





