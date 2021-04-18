---
title: Message WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ Status définit une fonction de rappel d’État dans l’application. AVICap appelle cette procédure à chaque modification de l’état de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- Message WM_CAP_SET_CALLBACK_STATUS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464491"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="4f457-106">\_Message d' \_ \_ État de rappel \_ de la définition de l’embout WM</span><span class="sxs-lookup"><span data-stu-id="4f457-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="4f457-107">Le message **WM \_ Cap \_ Set \_ callback \_ Status** définit une fonction de rappel d’État dans l’application.</span><span class="sxs-lookup"><span data-stu-id="4f457-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="4f457-108">AVICap appelle cette procédure à chaque modification de l’état de la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="4f457-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="4f457-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="4f457-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="4f457-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f457-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f457-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="4f457-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="4f457-112">Pointeur vers la fonction de rappel d’État, de type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span><span class="sxs-lookup"><span data-stu-id="4f457-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="4f457-113">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel d’état précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="4f457-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f457-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4f457-114">Return Value</span></span>

<span data-ttu-id="4f457-115">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="4f457-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f457-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4f457-116">Remarks</span></span>

<span data-ttu-id="4f457-117">Les applications peuvent éventuellement définir une fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="4f457-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="4f457-118">Si cette valeur est définie, AVICap appelle cette procédure dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="4f457-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="4f457-119">Une session de capture est terminée.</span><span class="sxs-lookup"><span data-stu-id="4f457-119">A capture session is completed.</span></span>
-   <span data-ttu-id="4f457-120">Un pilote de capture s’est correctement connecté à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="4f457-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="4f457-121">Une palette optimale est créée.</span><span class="sxs-lookup"><span data-stu-id="4f457-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="4f457-122">Le nombre de frames capturés est signalé.</span><span class="sxs-lookup"><span data-stu-id="4f457-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f457-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f457-123">Requirements</span></span>



| <span data-ttu-id="4f457-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f457-124">Requirement</span></span> | <span data-ttu-id="4f457-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f457-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4f457-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f457-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4f457-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f457-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4f457-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f457-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4f457-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f457-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4f457-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f457-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f457-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f457-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f457-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f457-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f457-133">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="4f457-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4f457-134">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="4f457-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





