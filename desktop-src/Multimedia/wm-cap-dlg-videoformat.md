---
title: Message WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEOFORMAT affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner le format vidéo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- Message WM_CAP_DLG_VIDEOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942003"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="8d6a3-104">\_Message WM Cap \_ DLG \_ VIDEOFORMAT</span><span class="sxs-lookup"><span data-stu-id="8d6a3-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="8d6a3-105">Le message **WM \_ Cap \_ DLG \_ VIDEOFORMAT** affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner le format vidéo.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="8d6a3-106">La boîte de dialogue Format vidéo peut être utilisée pour sélectionner les dimensions d’image, la profondeur de bit et les options de compression matérielle.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="8d6a3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="8d6a3-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="8d6a3-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8d6a3-108">Return Value</span></span>

<span data-ttu-id="8d6a3-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d6a3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8d6a3-110">Remarks</span></span>

<span data-ttu-id="8d6a3-111">Une fois ce message retourné, les applications devront peut-être mettre à jour la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) car l’utilisateur a peut-être modifié les dimensions de l’image.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="8d6a3-112">La boîte de dialogue Format vidéo est unique pour chaque pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="8d6a3-113">Certains pilotes de capture peuvent ne pas prendre en charge la boîte de dialogue Format vidéo.</span><span class="sxs-lookup"><span data-stu-id="8d6a3-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="8d6a3-114">Les applications peuvent déterminer si le pilote de capture prend en charge ce message en vérifiant le membre **fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span><span class="sxs-lookup"><span data-stu-id="8d6a3-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d6a3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d6a3-115">Requirements</span></span>



| <span data-ttu-id="8d6a3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d6a3-116">Requirement</span></span> | <span data-ttu-id="8d6a3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d6a3-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8d6a3-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d6a3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8d6a3-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d6a3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d6a3-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d6a3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8d6a3-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d6a3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d6a3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d6a3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d6a3-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d6a3-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d6a3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d6a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d6a3-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8d6a3-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8d6a3-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8d6a3-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





