---
title: Message WM_CAP_GET_STATUS (VFW. h)
description: Le \_ message WM Cap \_ obtenir \_ l’État récupère l’état de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- Message WM_CAP_GET_STATUS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032322"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="e426e-105">Message d’état de l' \_ \_ extraction WM \_</span><span class="sxs-lookup"><span data-stu-id="e426e-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="e426e-106">Le message **WM \_ Cap obtenir l' \_ \_ État** récupère l’état de la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="e426e-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="e426e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .</span><span class="sxs-lookup"><span data-stu-id="e426e-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="e426e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e426e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e426e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="e426e-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e426e-110">Taille, en octets, de la structure référencée par **s**.</span><span class="sxs-lookup"><span data-stu-id="e426e-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="e426e-111"><span id="s"></span><span id="S"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="e426e-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="e426e-112">Pointeur vers une structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .</span><span class="sxs-lookup"><span data-stu-id="e426e-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e426e-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e426e-113">Return Value</span></span>

<span data-ttu-id="e426e-114">Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="e426e-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="e426e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e426e-115">Remarks</span></span>

<span data-ttu-id="e426e-116">La structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contient l’état actuel de la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="e426e-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="e426e-117">Étant donné que cet État est dynamique et change en réponse à différents messages, l’application doit initialiser cette structure après avoir envoyé le message [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou à l’aide de la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) et chaque fois qu’il doit activer les éléments de menu ou déterminer l’état réel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e426e-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e426e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e426e-118">Requirements</span></span>



| <span data-ttu-id="e426e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e426e-119">Requirement</span></span> | <span data-ttu-id="e426e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e426e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e426e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e426e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e426e-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e426e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e426e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e426e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e426e-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e426e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e426e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e426e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e426e-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e426e-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e426e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e426e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e426e-128">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="e426e-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e426e-129">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="e426e-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





