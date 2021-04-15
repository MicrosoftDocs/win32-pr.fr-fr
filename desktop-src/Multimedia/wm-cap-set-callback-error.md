---
title: Message WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: Le \_ \_ \_ message d’erreur WM Cap Set callback \_ définit une fonction de rappel d’erreur dans l’application cliente. AVICap appelle cette procédure lorsque des erreurs se produisent. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- Message WM_CAP_SET_CALLBACK_ERROR Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465662"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="fd04e-106">Message d’erreur de rappel de l' \_ \_ ensemble de connexions WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd04e-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="fd04e-107">Le message d' **\_ erreur WM Cap \_ Set \_ callback \_** définit une fonction de rappel d’erreur dans l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="fd04e-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="fd04e-108">AVICap appelle cette procédure lorsque des erreurs se produisent.</span><span class="sxs-lookup"><span data-stu-id="fd04e-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="fd04e-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="fd04e-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="fd04e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd04e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd04e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="fd04e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="fd04e-112">Pointeur vers la fonction de rappel d’erreur, de type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span><span class="sxs-lookup"><span data-stu-id="fd04e-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="fd04e-113">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel d’erreur précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="fd04e-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd04e-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd04e-114">Return Value</span></span>

<span data-ttu-id="fd04e-115">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="fd04e-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd04e-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fd04e-116">Remarks</span></span>

<span data-ttu-id="fd04e-117">Les applications peuvent éventuellement définir une fonction de rappel d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fd04e-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="fd04e-118">Si cette valeur est définie, AVICap appelle la procédure d’erreur dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd04e-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="fd04e-119">Le disque est plein.</span><span class="sxs-lookup"><span data-stu-id="fd04e-119">The disk is full.</span></span>
-   <span data-ttu-id="fd04e-120">Une fenêtre de capture ne peut pas être connectée à un pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="fd04e-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="fd04e-121">Impossible d’ouvrir un appareil Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="fd04e-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="fd04e-122">Le nombre de trames supprimées pendant la capture dépasse le pourcentage spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd04e-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="fd04e-123">Les trames ne peuvent pas être capturées en raison de problèmes d’interruption de synchronisation verticale.</span><span class="sxs-lookup"><span data-stu-id="fd04e-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd04e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd04e-124">Requirements</span></span>



| <span data-ttu-id="fd04e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd04e-125">Requirement</span></span> | <span data-ttu-id="fd04e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd04e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fd04e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd04e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fd04e-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd04e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fd04e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd04e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fd04e-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd04e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fd04e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd04e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd04e-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd04e-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd04e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd04e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd04e-134">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="fd04e-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fd04e-135">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="fd04e-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





