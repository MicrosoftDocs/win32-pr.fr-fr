---
title: Message WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEOSOURCE affiche une boîte de dialogue dans laquelle l’utilisateur peut contrôler la source vidéo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- Message WM_CAP_DLG_VIDEOSOURCE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464978"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="219d6-104">\_Message WM Cap \_ DLG \_ VIDEOSOURCE</span><span class="sxs-lookup"><span data-stu-id="219d6-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="219d6-105">Le message **WM \_ Cap \_ DLG \_ VIDEOSOURCE** affiche une boîte de dialogue dans laquelle l’utilisateur peut contrôler la source vidéo.</span><span class="sxs-lookup"><span data-stu-id="219d6-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="219d6-106">La boîte de dialogue source vidéo peut contenir des contrôles qui sélectionnent des sources d’entrée. Modifiez la teinte, le contraste et la luminosité de l’image. et modifiez la qualité vidéo avant de numériser les images dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="219d6-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="219d6-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .</span><span class="sxs-lookup"><span data-stu-id="219d6-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="219d6-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="219d6-108">Return Value</span></span>

<span data-ttu-id="219d6-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="219d6-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="219d6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="219d6-110">Remarks</span></span>

<span data-ttu-id="219d6-111">La boîte de dialogue source vidéo est unique pour chaque pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="219d6-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="219d6-112">Certains pilotes de capture peuvent ne pas prendre en charge une boîte de dialogue source vidéo.</span><span class="sxs-lookup"><span data-stu-id="219d6-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="219d6-113">Les applications peuvent déterminer si le pilote de capture prend en charge ce message en vérifiant le membre **fHasDlgVideoSource** de la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="219d6-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="219d6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="219d6-114">Requirements</span></span>



| <span data-ttu-id="219d6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="219d6-115">Requirement</span></span> | <span data-ttu-id="219d6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="219d6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="219d6-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="219d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="219d6-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="219d6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="219d6-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="219d6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="219d6-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="219d6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="219d6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="219d6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="219d6-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="219d6-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="219d6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="219d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219d6-124">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="219d6-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="219d6-125">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="219d6-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





