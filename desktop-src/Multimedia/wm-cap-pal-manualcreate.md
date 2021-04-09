---
title: Message WM_CAP_PAL_MANUALCREATE (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ MANUALCREATE demande que le pilote de capture échantillonne manuellement les images vidéo et crée une nouvelle palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- Message WM_CAP_PAL_MANUALCREATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740957"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="c53e9-105">\_Message WM Cap \_ PAL \_ MANUALCREATE</span><span class="sxs-lookup"><span data-stu-id="c53e9-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="c53e9-106">Le message **WM \_ Cap \_ PAL \_ MANUALCREATE** demande que le pilote de capture échantillonne manuellement les images vidéo et crée une nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="c53e9-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="c53e9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .</span><span class="sxs-lookup"><span data-stu-id="c53e9-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="c53e9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c53e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c53e9-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span><span class="sxs-lookup"><span data-stu-id="c53e9-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="c53e9-110">Indicateur d’histogramme de la palette.</span><span class="sxs-lookup"><span data-stu-id="c53e9-110">Palette histogram flag.</span></span> <span data-ttu-id="c53e9-111">Définissez ce paramètre sur **true** pour chaque frame inclus dans la création de la palette optimale.</span><span class="sxs-lookup"><span data-stu-id="c53e9-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="c53e9-112">Après avoir collecté la dernière trame, définissez ce paramètre sur **false** pour calculer la palette optimale et l’envoyer au pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="c53e9-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="c53e9-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="c53e9-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="c53e9-114">Nombre de couleurs dans la palette.</span><span class="sxs-lookup"><span data-stu-id="c53e9-114">Number of colors in the palette.</span></span> <span data-ttu-id="c53e9-115">La valeur maximale de ce paramètre est 256.</span><span class="sxs-lookup"><span data-stu-id="c53e9-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="c53e9-116">Cette valeur est utilisée uniquement pendant la collecte de la première image d’une séquence.</span><span class="sxs-lookup"><span data-stu-id="c53e9-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c53e9-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c53e9-117">Return Value</span></span>

<span data-ttu-id="c53e9-118">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c53e9-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="c53e9-119">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="c53e9-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c53e9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c53e9-120">Requirements</span></span>



| <span data-ttu-id="c53e9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c53e9-121">Requirement</span></span> | <span data-ttu-id="c53e9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c53e9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c53e9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c53e9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c53e9-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c53e9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c53e9-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c53e9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c53e9-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c53e9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c53e9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c53e9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c53e9-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c53e9-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c53e9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c53e9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c53e9-130">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="c53e9-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c53e9-131">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="c53e9-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





