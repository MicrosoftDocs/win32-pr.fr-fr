---
title: Message WM_CAP_SET_SCALE (VFW. h)
description: Le \_ message WM embout \_ Set \_ Scale active ou désactive la mise à l’échelle des images vidéo en préversion.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- Message WM_CAP_SET_SCALE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106111"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="ec32b-104">Message de mise à l’échelle du jeu de \_ connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="ec32b-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="ec32b-105">Le message **WM \_ embout \_ Set \_ Scale** active ou désactive la mise à l’échelle des images vidéo en préversion.</span><span class="sxs-lookup"><span data-stu-id="ec32b-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="ec32b-106">Si la mise à l’échelle est activée, l’image vidéo capturée est étirée sur les dimensions de la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="ec32b-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="ec32b-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .</span><span class="sxs-lookup"><span data-stu-id="ec32b-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="ec32b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec32b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec32b-109"><span id="f"></span><span id="F"></span>*FA*</span><span class="sxs-lookup"><span data-stu-id="ec32b-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="ec32b-110">Indicateur de mise à l’échelle de l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="ec32b-110">Preview scaling flag.</span></span> <span data-ttu-id="ec32b-111">Spécifiez **true** pour que ce paramètre étire les images d’aperçu à la taille de la fenêtre de capture ou **false** pour les afficher à leur taille naturelle.</span><span class="sxs-lookup"><span data-stu-id="ec32b-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec32b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec32b-112">Return Value</span></span>

<span data-ttu-id="ec32b-113">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ec32b-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec32b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ec32b-114">Remarks</span></span>

<span data-ttu-id="ec32b-115">La mise à l’échelle des images d’aperçu contrôle la présentation immédiate des frames capturés dans la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="ec32b-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="ec32b-116">Elle n’a aucun effet sur la taille des frames enregistrés dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="ec32b-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="ec32b-117">La mise à l’échelle n’a aucun effet lors de l’utilisation de la superposition pour afficher la vidéo dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="ec32b-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec32b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec32b-118">Requirements</span></span>



| <span data-ttu-id="ec32b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec32b-119">Requirement</span></span> | <span data-ttu-id="ec32b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec32b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec32b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec32b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ec32b-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec32b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec32b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec32b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ec32b-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec32b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec32b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec32b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec32b-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec32b-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec32b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec32b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec32b-128">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="ec32b-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ec32b-129">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="ec32b-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





