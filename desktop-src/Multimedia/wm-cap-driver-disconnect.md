---
title: Message WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: Le \_ message de \_ déconnexion du pilote WM Cap \_ déconnecte un pilote de capture d’une fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- Message WM_CAP_DRIVER_DISCONNECT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942002"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="caf05-105">\_Message de \_ déconnexion du pilote WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="caf05-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="caf05-106">Le message de **\_ \_ \_ déconnexion du pilote WM Cap** déconnecte un pilote de capture d’une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="caf05-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="caf05-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .</span><span class="sxs-lookup"><span data-stu-id="caf05-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="caf05-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="caf05-108">Return Value</span></span>

<span data-ttu-id="caf05-109">Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="caf05-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="caf05-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caf05-110">Requirements</span></span>



| <span data-ttu-id="caf05-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caf05-111">Requirement</span></span> | <span data-ttu-id="caf05-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="caf05-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="caf05-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caf05-113">Minimum supported client</span></span><br/> | <span data-ttu-id="caf05-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caf05-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="caf05-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caf05-115">Minimum supported server</span></span><br/> | <span data-ttu-id="caf05-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caf05-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="caf05-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="caf05-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="caf05-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="caf05-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caf05-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caf05-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf05-120">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="caf05-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="caf05-121">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="caf05-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





