---
title: Message WM_CAP_GRAB_FRAME (VFW. h)
description: Le \_ message de \_ Frame de capture du capuchon WM \_ récupère et affiche une image unique du pilote de capture. Après la capture, la superposition et l’aperçu sont désactivés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- Message WM_CAP_GRAB_FRAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465666"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="df76f-106">\_Message du \_ Frame de capture du capuchon WM \_</span><span class="sxs-lookup"><span data-stu-id="df76f-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="df76f-107">Le message de **\_ \_ \_ Frame** de capture du capuchon WM récupère et affiche une image unique du pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="df76f-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="df76f-108">Après la capture, la superposition et l’aperçu sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="df76f-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="df76f-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .</span><span class="sxs-lookup"><span data-stu-id="df76f-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="df76f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df76f-110">Return Value</span></span>

<span data-ttu-id="df76f-111">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="df76f-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df76f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="df76f-112">Remarks</span></span>

<span data-ttu-id="df76f-113">Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="df76f-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="df76f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df76f-114">Requirements</span></span>



| <span data-ttu-id="df76f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df76f-115">Requirement</span></span> | <span data-ttu-id="df76f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="df76f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df76f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df76f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df76f-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df76f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df76f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df76f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df76f-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df76f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df76f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="df76f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="df76f-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="df76f-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df76f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df76f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df76f-124">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="df76f-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="df76f-125">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="df76f-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





