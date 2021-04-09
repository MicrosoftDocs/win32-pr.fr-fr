---
title: Message WM_CAP_SINGLE_FRAME (VFW. h)
description: Le \_ message WM Cap \_ Single \_ Frame ajoute une image unique à un fichier de capture qui a été ouvert à l’aide du message d’ouverture du \_ \_ cadre unique WM Cap \_ \_ . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- Message WM_CAP_SINGLE_FRAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106099"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="7d187-105">\_Message de \_ Frame unique WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="7d187-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="7d187-106">Le message **WM \_ Cap \_ Single \_ Frame** ajoute une image unique à un fichier de capture qui a été ouvert à l’aide du message d' [**\_ \_ \_ \_ ouverture du cadre unique WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7d187-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="7d187-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .</span><span class="sxs-lookup"><span data-stu-id="7d187-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="7d187-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7d187-108">Return Value</span></span>

<span data-ttu-id="7d187-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7d187-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d187-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d187-110">Requirements</span></span>



| <span data-ttu-id="7d187-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d187-111">Requirement</span></span> | <span data-ttu-id="7d187-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d187-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7d187-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d187-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7d187-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d187-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7d187-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d187-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7d187-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d187-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7d187-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d187-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d187-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d187-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d187-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d187-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d187-120">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="7d187-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7d187-121">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="7d187-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





