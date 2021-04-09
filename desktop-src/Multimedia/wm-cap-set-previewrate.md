---
title: Message WM_CAP_SET_PREVIEWRATE (VFW. h)
description: Le \_ message WM Cap \_ Set \_ PREVIEWRATE définit la fréquence d’affichage des frames en mode aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- Message WM_CAP_SET_PREVIEWRATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942794"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="7467c-105">\_Message PREVIEWRATE de l’ensemble de connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="7467c-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="7467c-106">Le message **WM \_ Cap \_ Set \_ PREVIEWRATE** définit la fréquence d’affichage des frames en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="7467c-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="7467c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .</span><span class="sxs-lookup"><span data-stu-id="7467c-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="7467c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7467c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7467c-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span><span class="sxs-lookup"><span data-stu-id="7467c-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="7467c-110">Vitesse, en millisecondes, à laquelle les nouveaux frames sont capturés et affichés.</span><span class="sxs-lookup"><span data-stu-id="7467c-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7467c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7467c-111">Return Value</span></span>

<span data-ttu-id="7467c-112">Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="7467c-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="7467c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7467c-113">Remarks</span></span>

<span data-ttu-id="7467c-114">Le mode aperçu utilise des ressources processeur importantes.</span><span class="sxs-lookup"><span data-stu-id="7467c-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="7467c-115">Les applications peuvent désactiver l’aperçu ou réduire le taux d’aperçu lorsqu’une autre application a le focus.</span><span class="sxs-lookup"><span data-stu-id="7467c-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="7467c-116">Pendant la capture vidéo en continu, la tâche d’aperçu est moins prioritaire que l’écriture d’images sur le disque, et les images d’aperçu ne sont affichées que si aucune autre mémoire tampon n’est disponible pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="7467c-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7467c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7467c-117">Requirements</span></span>



| <span data-ttu-id="7467c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7467c-118">Requirement</span></span> | <span data-ttu-id="7467c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7467c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7467c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7467c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7467c-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7467c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7467c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7467c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7467c-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7467c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7467c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7467c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7467c-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7467c-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7467c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7467c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7467c-127">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="7467c-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7467c-128">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="7467c-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





