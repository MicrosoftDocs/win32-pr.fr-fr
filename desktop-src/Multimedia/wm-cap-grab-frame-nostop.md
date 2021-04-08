---
title: Message WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: Le \_ \_ message nostop de la trame de manipulation du capuchon WM \_ \_ remplit la mémoire tampon de trame avec un seul frame non compressé à partir du périphérique de capture et l’affiche.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- Message WM_CAP_GRAB_FRAME_NOSTOP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844065"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="067d8-104">\_ \_ \_ Message nostop de la trame de manipulation de l’embout WM \_</span><span class="sxs-lookup"><span data-stu-id="067d8-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="067d8-105">Le **message \_ \_ \_ \_ nostop de la trame de manipulation du capuchon WM** remplit la mémoire tampon de trame avec un seul frame non compressé à partir du périphérique de capture et l’affiche.</span><span class="sxs-lookup"><span data-stu-id="067d8-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="067d8-106">Contrairement au message [**de \_ \_ \_ trame de manipulation de l’embout WM**](wm-cap-grab-frame.md) , l’état de la superposition ou de l’aperçu n’est pas modifié par ce message.</span><span class="sxs-lookup"><span data-stu-id="067d8-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="067d8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .</span><span class="sxs-lookup"><span data-stu-id="067d8-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="067d8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="067d8-108">Return Value</span></span>

<span data-ttu-id="067d8-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="067d8-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="067d8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="067d8-110">Remarks</span></span>

<span data-ttu-id="067d8-111">Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="067d8-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="067d8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="067d8-112">Requirements</span></span>



| <span data-ttu-id="067d8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="067d8-113">Requirement</span></span> | <span data-ttu-id="067d8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="067d8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="067d8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="067d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="067d8-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="067d8-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="067d8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="067d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="067d8-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="067d8-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="067d8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="067d8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="067d8-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="067d8-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="067d8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="067d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067d8-122">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="067d8-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="067d8-123">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="067d8-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





