---
title: Message WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: Le \_ message de \_ fermeture de frame unique WM capuchon \_ \_ ferme le fichier de capture ouvert par le \_ message d’ouverture du \_ cadre unique WM Cap \_ \_ . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- Message WM_CAP_SINGLE_FRAME_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743548"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="cbf00-105">\_Message de \_ \_ fermeture de frame unique WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="cbf00-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="cbf00-106">Le message de **\_ \_ \_ \_ fermeture de frame unique WM capuchon** ferme le fichier de capture ouvert par le message d' [**\_ \_ \_ \_ ouverture du cadre unique WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="cbf00-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="cbf00-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .</span><span class="sxs-lookup"><span data-stu-id="cbf00-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="cbf00-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cbf00-108">Return Value</span></span>

<span data-ttu-id="cbf00-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="cbf00-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf00-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cbf00-110">Remarks</span></span>

<span data-ttu-id="cbf00-111">Pour plus d’informations sur l’installation des fonctions de rappel, consultez les messages d' [**\_ erreur WM Cap \_ Set \_ callback \_ Error**](wm-cap-set-callback-error.md) et [**WM \_ Cap \_ Set \_ callback \_ Frame**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="cbf00-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbf00-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbf00-112">Requirements</span></span>



| <span data-ttu-id="cbf00-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbf00-113">Requirement</span></span> | <span data-ttu-id="cbf00-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbf00-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cbf00-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbf00-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf00-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbf00-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cbf00-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbf00-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf00-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbf00-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cbf00-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbf00-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbf00-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf00-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf00-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbf00-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf00-122">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="cbf00-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cbf00-123">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="cbf00-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





