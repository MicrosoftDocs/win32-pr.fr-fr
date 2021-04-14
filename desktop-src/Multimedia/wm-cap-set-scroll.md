---
title: Message WM_CAP_SET_SCROLL (VFW. h)
description: Le \_ \_ \_ message de défilement WM Cap Set définit la partie de la trame vidéo à afficher dans la fenêtre de capture.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- Message WM_CAP_SET_SCROLL Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466866"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="52d3e-104">Message de défilement de l' \_ ensemble de connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="52d3e-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="52d3e-105">Le message de **\_ \_ \_ défilement WM Cap Set** définit la partie de la trame vidéo à afficher dans la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="52d3e-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="52d3e-106">Ce message définit l’angle supérieur gauche de la zone cliente de la fenêtre de capture sur les coordonnées d’un pixel spécifié dans le cadre de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="52d3e-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="52d3e-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="52d3e-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="52d3e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52d3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d3e-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span><span class="sxs-lookup"><span data-stu-id="52d3e-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="52d3e-110">Adresse qui doit contenir la position de défilement souhaitée.</span><span class="sxs-lookup"><span data-stu-id="52d3e-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d3e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="52d3e-111">Return Value</span></span>

<span data-ttu-id="52d3e-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="52d3e-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d3e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="52d3e-113">Remarks</span></span>

<span data-ttu-id="52d3e-114">La position de défilement affecte l’image dans les modes d’aperçu et de superposition.</span><span class="sxs-lookup"><span data-stu-id="52d3e-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="52d3e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52d3e-115">Requirements</span></span>



| <span data-ttu-id="52d3e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52d3e-116">Requirement</span></span> | <span data-ttu-id="52d3e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d3e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="52d3e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d3e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52d3e-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d3e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="52d3e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d3e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52d3e-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d3e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="52d3e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="52d3e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d3e-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d3e-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d3e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52d3e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d3e-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="52d3e-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="52d3e-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="52d3e-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





