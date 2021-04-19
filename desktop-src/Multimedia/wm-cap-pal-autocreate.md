---
title: Message WM_CAP_PAL_AUTOCREATE (VFW. h)
description: Le \_ message de \_ création automatique WM Cap PAL \_ demande que le pilote de capture échantillonne les images vidéo et crée automatiquement une nouvelle palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- Message WM_CAP_PAL_AUTOCREATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510743"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="84339-105">Message de création d’un \_ \_ message d’attente PAL PAC \_</span><span class="sxs-lookup"><span data-stu-id="84339-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="84339-106">Le message de **création automatique WM \_ Cap \_ PAL \_** demande que le pilote de capture échantillonne les images vidéo et crée automatiquement une nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="84339-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="84339-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .</span><span class="sxs-lookup"><span data-stu-id="84339-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="84339-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84339-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84339-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="84339-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="84339-110">Nombre d’images à échantillonner.</span><span class="sxs-lookup"><span data-stu-id="84339-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="84339-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="84339-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="84339-112">Nombre de couleurs dans la palette.</span><span class="sxs-lookup"><span data-stu-id="84339-112">Number of colors in the palette.</span></span> <span data-ttu-id="84339-113">La valeur maximale de ce paramètre est 256.</span><span class="sxs-lookup"><span data-stu-id="84339-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84339-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84339-114">Return Value</span></span>

<span data-ttu-id="84339-115">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84339-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="84339-116">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="84339-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="84339-117">Notes</span><span class="sxs-lookup"><span data-stu-id="84339-117">Remarks</span></span>

<span data-ttu-id="84339-118">La séquence vidéo échantillonnée doit inclure toutes les couleurs souhaitées dans la palette.</span><span class="sxs-lookup"><span data-stu-id="84339-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="84339-119">Pour obtenir la meilleure palette, vous devrez peut-être échantillonner l’intégralité de la séquence plutôt qu’une partie de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="84339-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="84339-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84339-120">Requirements</span></span>



| <span data-ttu-id="84339-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84339-121">Requirement</span></span> | <span data-ttu-id="84339-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="84339-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84339-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84339-123">Minimum supported client</span></span><br/> | <span data-ttu-id="84339-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84339-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84339-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84339-125">Minimum supported server</span></span><br/> | <span data-ttu-id="84339-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84339-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84339-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="84339-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="84339-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="84339-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84339-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84339-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84339-130">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="84339-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="84339-131">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="84339-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





