---
title: Message WM_CAP_ABORT (VFW. h)
description: Le \_ message WM Cap \_ Abort arrête l’opération de capture.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- Message WM_CAP_ABORT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508538"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="5a257-104">\_Message WM Cap \_ Abort</span><span class="sxs-lookup"><span data-stu-id="5a257-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="5a257-105">Le message **WM \_ Cap \_ Abort** arrête l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="5a257-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="5a257-106">Dans le cas de la capture de l’étape, les données d’image collectées jusqu’au point du message **WM \_ Cap \_ Abort** sont conservées dans le fichier de capture, mais l’audio n’est pas capturé.</span><span class="sxs-lookup"><span data-stu-id="5a257-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="5a257-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .</span><span class="sxs-lookup"><span data-stu-id="5a257-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="5a257-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a257-108">Return Value</span></span>

<span data-ttu-id="5a257-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5a257-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a257-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5a257-110">Remarks</span></span>

<span data-ttu-id="5a257-111">L’opération de capture doit donner l’utilisation de ce message.</span><span class="sxs-lookup"><span data-stu-id="5a257-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="5a257-112">Utilisez le message [**WM \_ Cap \_ Stop**](wm-cap-stop.md) pour interrompre la capture de l’étape à la position actuelle, puis capturez l’audio.</span><span class="sxs-lookup"><span data-stu-id="5a257-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a257-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a257-113">Requirements</span></span>



| <span data-ttu-id="5a257-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a257-114">Requirement</span></span> | <span data-ttu-id="5a257-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a257-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5a257-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a257-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a257-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a257-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5a257-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a257-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a257-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a257-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5a257-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a257-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a257-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a257-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a257-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a257-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a257-123">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="5a257-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="5a257-124">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="5a257-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





