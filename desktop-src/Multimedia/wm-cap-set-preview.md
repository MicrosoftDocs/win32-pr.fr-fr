---
title: Message WM_CAP_SET_PREVIEW (VFW. h)
description: Le \_ message WM Cap \_ Set \_ preview active ou désactive le mode aperçu.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- Message WM_CAP_SET_PREVIEW Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106114"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="594e2-104">Message d’aperçu de l' \_ ensemble de connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="594e2-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="594e2-105">Le message **WM \_ Cap \_ Set \_ preview** active ou désactive le mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="594e2-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="594e2-106">En mode aperçu, les frames sont transférés du matériel de capture à la mémoire système, puis affichés dans la fenêtre de capture à l’aide des fonctions GDI.</span><span class="sxs-lookup"><span data-stu-id="594e2-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="594e2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .</span><span class="sxs-lookup"><span data-stu-id="594e2-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="594e2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="594e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594e2-109"><span id="f"></span><span id="F"></span>*FA*</span><span class="sxs-lookup"><span data-stu-id="594e2-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="594e2-110">Indicateur d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="594e2-110">Preview flag.</span></span> <span data-ttu-id="594e2-111">Spécifiez **true** pour ce paramètre pour activer le mode aperçu ou **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="594e2-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="594e2-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="594e2-112">Return Value</span></span>

<span data-ttu-id="594e2-113">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="594e2-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="594e2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="594e2-114">Remarks</span></span>

<span data-ttu-id="594e2-115">Le mode aperçu utilise des ressources processeur importantes.</span><span class="sxs-lookup"><span data-stu-id="594e2-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="594e2-116">Les applications peuvent désactiver l’aperçu ou réduire le taux d’aperçu lorsqu’une autre application a le focus.</span><span class="sxs-lookup"><span data-stu-id="594e2-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="594e2-117">Le membre **fLiveWindow** de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indique si le mode aperçu est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="594e2-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="594e2-118">L’activation du mode aperçu désactive automatiquement le mode superposition.</span><span class="sxs-lookup"><span data-stu-id="594e2-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="594e2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="594e2-119">Requirements</span></span>



| <span data-ttu-id="594e2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="594e2-120">Requirement</span></span> | <span data-ttu-id="594e2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="594e2-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="594e2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="594e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="594e2-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="594e2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="594e2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="594e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="594e2-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="594e2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="594e2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="594e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="594e2-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="594e2-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="594e2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="594e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594e2-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="594e2-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="594e2-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="594e2-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





