---
title: Message WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: Le \_ \_ \_ message d’ouverture du frame unique WM Cap \_ ouvre le fichier de capture pour la capture d’une seule image. Toutes les informations précédentes du fichier de capture sont remplacées. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- Message WM_CAP_SINGLE_FRAME_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844282"
---
# <a name="wm_cap_single_frame_open-message"></a><span data-ttu-id="cc296-106">\_Message d' \_ ouverture d’un frame unique WM Cap \_ \_</span><span class="sxs-lookup"><span data-stu-id="cc296-106">WM\_CAP\_SINGLE\_FRAME\_OPEN message</span></span>

<span data-ttu-id="cc296-107">Le message d' **\_ \_ \_ \_ ouverture du frame unique WM Cap** ouvre le fichier de capture pour la capture d’une seule image.</span><span class="sxs-lookup"><span data-stu-id="cc296-107">The **WM\_CAP\_SINGLE\_FRAME\_OPEN** message opens the capture file for single-frame capturing.</span></span> <span data-ttu-id="cc296-108">Toutes les informations précédentes du fichier de capture sont remplacées.</span><span class="sxs-lookup"><span data-stu-id="cc296-108">Any previous information in the capture file is overwritten.</span></span> <span data-ttu-id="cc296-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .</span><span class="sxs-lookup"><span data-stu-id="cc296-109">You can send this message explicitly or by using the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="cc296-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc296-110">Return Value</span></span>

<span data-ttu-id="cc296-111">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cc296-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc296-112">Notes</span><span class="sxs-lookup"><span data-stu-id="cc296-112">Remarks</span></span>

<span data-ttu-id="cc296-113">Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="cc296-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc296-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc296-114">Requirements</span></span>



| <span data-ttu-id="cc296-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc296-115">Requirement</span></span> | <span data-ttu-id="cc296-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc296-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cc296-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc296-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc296-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc296-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cc296-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc296-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc296-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc296-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc296-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc296-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc296-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc296-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc296-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc296-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc296-124">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="cc296-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cc296-125">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="cc296-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





