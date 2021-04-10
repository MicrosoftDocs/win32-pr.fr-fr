---
title: Message WM_CAP_PAL_PASTE (VFW. h)
description: Le \_ message WM Cap \_ PAL \_ Paste copie la palette à partir du presse-papiers et la transmet à un pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- Message WM_CAP_PAL_PASTE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941927"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="8b395-105">\_Coller le message WM capuchon \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="8b395-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="8b395-106">Le message **WM \_ Cap \_ PAL \_ Paste** copie la palette à partir du presse-papiers et la transmet à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="8b395-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="8b395-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .</span><span class="sxs-lookup"><span data-stu-id="8b395-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="8b395-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b395-108">Return Value</span></span>

<span data-ttu-id="8b395-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8b395-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="8b395-110">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="8b395-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b395-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8b395-111">Remarks</span></span>

<span data-ttu-id="8b395-112">Un pilote de capture utilise une palette lorsqu’il est requis par le format vidéo numérisé spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b395-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b395-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b395-113">Requirements</span></span>



| <span data-ttu-id="8b395-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b395-114">Requirement</span></span> | <span data-ttu-id="8b395-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b395-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8b395-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b395-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b395-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b395-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8b395-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b395-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b395-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b395-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8b395-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b395-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b395-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b395-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b395-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b395-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b395-123">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8b395-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8b395-124">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="8b395-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





