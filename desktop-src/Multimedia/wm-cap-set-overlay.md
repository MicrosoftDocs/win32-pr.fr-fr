---
title: Message WM_CAP_SET_OVERLAY (VFW. h)
description: Le \_ message WM Cap \_ Set \_ Overlay active ou désactive le mode superposition. En mode superposition, la vidéo est affichée à l’aide de la superposition matérielle. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- Message WM_CAP_SET_OVERLAY Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512206"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="c979b-106">\_Message de \_ superposition du jeu de bouchon WM \_</span><span class="sxs-lookup"><span data-stu-id="c979b-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="c979b-107">Le message **WM \_ Cap \_ Set \_ Overlay** active ou désactive le mode superposition.</span><span class="sxs-lookup"><span data-stu-id="c979b-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="c979b-108">En mode superposition, la vidéo est affichée à l’aide de la superposition matérielle.</span><span class="sxs-lookup"><span data-stu-id="c979b-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="c979b-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .</span><span class="sxs-lookup"><span data-stu-id="c979b-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="c979b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c979b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c979b-111"><span id="f"></span><span id="F"></span>*FA*</span><span class="sxs-lookup"><span data-stu-id="c979b-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="c979b-112">Indicateur de superposition.</span><span class="sxs-lookup"><span data-stu-id="c979b-112">Overlay flag.</span></span> <span data-ttu-id="c979b-113">Spécifiez **true** pour ce paramètre pour activer le mode de superposition ou **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="c979b-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c979b-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c979b-114">Return Value</span></span>

<span data-ttu-id="c979b-115">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c979b-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c979b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c979b-116">Remarks</span></span>

<span data-ttu-id="c979b-117">L’utilisation d’une superposition ne requiert pas de ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="c979b-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="c979b-118">Le membre **fHasOverlay** de la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indique si l’appareil est en capacité de se superposer.</span><span class="sxs-lookup"><span data-stu-id="c979b-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="c979b-119">Le membre **fOverlayWindow** de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indique si le mode superposition est actuellement activé.</span><span class="sxs-lookup"><span data-stu-id="c979b-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="c979b-120">L’activation du mode superposition désactive automatiquement le mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="c979b-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="c979b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c979b-121">Requirements</span></span>



| <span data-ttu-id="c979b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c979b-122">Requirement</span></span> | <span data-ttu-id="c979b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c979b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c979b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c979b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c979b-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c979b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c979b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c979b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c979b-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c979b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c979b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c979b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c979b-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c979b-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c979b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c979b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c979b-131">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="c979b-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c979b-132">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="c979b-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





