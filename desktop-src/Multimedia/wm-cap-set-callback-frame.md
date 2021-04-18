---
title: Message WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ Frame définit une fonction de rappel d’aperçu dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture capture des images d’aperçu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- Message WM_CAP_SET_CALLBACK_FRAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536292"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="e7808-106">\_Message de \_ \_ \_ trame de rappel de la définition de l’embout WM</span><span class="sxs-lookup"><span data-stu-id="e7808-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="e7808-107">Le message **WM \_ Cap \_ Set \_ callback \_ Frame** définit une fonction de rappel d’aperçu dans l’application.</span><span class="sxs-lookup"><span data-stu-id="e7808-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="e7808-108">AVICap appelle cette procédure lorsque la fenêtre de capture capture des images d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="e7808-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="e7808-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="e7808-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="e7808-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7808-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7808-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="e7808-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="e7808-112">Pointeur vers la fonction de rappel d’aperçu, de type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="e7808-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="e7808-113">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="e7808-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7808-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e7808-114">Return Value</span></span>

<span data-ttu-id="e7808-115">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="e7808-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7808-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e7808-116">Remarks</span></span>

<span data-ttu-id="e7808-117">La fenêtre de capture appelle la fonction de rappel avant d’afficher des images d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="e7808-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="e7808-118">Cela permet à une application de modifier le frame si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="e7808-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="e7808-119">Cette fonction de rappel n’est pas utilisée pendant la capture vidéo en continu.</span><span class="sxs-lookup"><span data-stu-id="e7808-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7808-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7808-120">Requirements</span></span>



| <span data-ttu-id="e7808-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7808-121">Requirement</span></span> | <span data-ttu-id="e7808-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7808-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e7808-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7808-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7808-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7808-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e7808-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7808-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7808-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7808-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e7808-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7808-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7808-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7808-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7808-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7808-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7808-130">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="e7808-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e7808-131">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="e7808-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





