---
title: Message WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEODISPLAY affiche une boîte de dialogue dans laquelle l’utilisateur peut définir ou ajuster la sortie vidéo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- Message WM_CAP_DLG_VIDEODISPLAY Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942096"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="806d2-104">\_Message WM Cap \_ DLG \_ VIDEODISPLAY</span><span class="sxs-lookup"><span data-stu-id="806d2-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="806d2-105">Le message **WM \_ Cap \_ DLG \_ VIDEODISPLAY** affiche une boîte de dialogue dans laquelle l’utilisateur peut définir ou ajuster la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="806d2-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="806d2-106">Cette boîte de dialogue peut contenir des contrôles qui affectent la teinte, le contraste et la luminosité de l’image affichée, ainsi que l’alignement des couleurs des touches.</span><span class="sxs-lookup"><span data-stu-id="806d2-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="806d2-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .</span><span class="sxs-lookup"><span data-stu-id="806d2-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="806d2-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="806d2-108">Return Value</span></span>

<span data-ttu-id="806d2-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="806d2-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="806d2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="806d2-110">Remarks</span></span>

<span data-ttu-id="806d2-111">Les contrôles de cette boîte de dialogue n’affectent pas les données vidéo numérisées ; elles affectent uniquement la sortie ou le réaffichage du signal vidéo.</span><span class="sxs-lookup"><span data-stu-id="806d2-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="806d2-112">La boîte de dialogue affichage vidéo est unique pour chaque pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="806d2-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="806d2-113">Certains pilotes de capture peuvent ne pas prendre en charge une boîte de dialogue d’affichage vidéo.</span><span class="sxs-lookup"><span data-stu-id="806d2-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="806d2-114">Les applications peuvent déterminer si le pilote de capture prend en charge ce message en vérifiant le membre **fHasDlgVideoDisplay** de la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="806d2-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="806d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="806d2-115">Requirements</span></span>



| <span data-ttu-id="806d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="806d2-116">Requirement</span></span> | <span data-ttu-id="806d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="806d2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="806d2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="806d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="806d2-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="806d2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="806d2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="806d2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="806d2-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="806d2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="806d2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="806d2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="806d2-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="806d2-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="806d2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="806d2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806d2-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="806d2-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="806d2-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="806d2-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





