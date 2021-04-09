---
title: Message WM_CAP_EDIT_COPY (VFW. h)
description: Le \_ message WM Cap \_ Edit \_ Copy copie le contenu de la mémoire tampon de l’image vidéo et la palette associée dans le presse-papiers. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- Message WM_CAP_EDIT_COPY Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104701"
---
# <a name="wm_cap_edit_copy-message"></a><span data-ttu-id="152b5-105">Message WM- \_ \_ modifier la \_ copie</span><span class="sxs-lookup"><span data-stu-id="152b5-105">WM\_CAP\_EDIT\_COPY message</span></span>

<span data-ttu-id="152b5-106">Le message **WM \_ Cap \_ Edit \_ Copy** copie le contenu de la mémoire tampon de l’image vidéo et la palette associée dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="152b5-106">The **WM\_CAP\_EDIT\_COPY** message copies the contents of the video frame buffer and associated palette to the clipboard.</span></span> <span data-ttu-id="152b5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .</span><span class="sxs-lookup"><span data-stu-id="152b5-107">You can send this message explicitly or by using the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro.</span></span>


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="152b5-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="152b5-108">Return Value</span></span>

<span data-ttu-id="152b5-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="152b5-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="152b5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="152b5-110">Requirements</span></span>



| <span data-ttu-id="152b5-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="152b5-111">Requirement</span></span> | <span data-ttu-id="152b5-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="152b5-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="152b5-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="152b5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="152b5-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="152b5-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="152b5-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="152b5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="152b5-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="152b5-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="152b5-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="152b5-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="152b5-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="152b5-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152b5-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="152b5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152b5-120">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="152b5-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="152b5-121">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="152b5-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





