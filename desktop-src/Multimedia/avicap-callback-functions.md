---
title: Fonctions de rappel AVICap
description: Fonctions de rappel AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- AVICap, classe, fonctions de rappel
- Fonctions de rappel AVICap, à propos de
- Message WM_CAP_SET_CALLBACK_CAPCONTROL
- Message WM_CAP_SET_CALLBACK_ERROR
- Message WM_CAP_SET_CALLBACK_FRAME
- Message WM_CAP_SET_CALLBACK_STATUS
- Message WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Message WM_CAP_SET_CALLBACK_WAVESTREAM
- Message WM_CAP_SET_CALLBACK_YIELD
- capSetCallbackOnCapControl macro)
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame macro)
- capSetCallbackOnStatus macro)
- capSetCallbackOnVideoStream macro)
- capSetCallbackOnWaveStream macro)
- capSetCallbackOnYield macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940297"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="e2d92-119">Fonctions de rappel AVICap</span><span class="sxs-lookup"><span data-stu-id="e2d92-119">AVICap Callback Functions</span></span>

<span data-ttu-id="e2d92-120">Votre application peut inscrire des fonctions de rappel avec une fenêtre de capture pour qu’elle notifie votre application lorsque l’état change, lorsque des erreurs se produisent, lorsque des mémoires tampons audio et vidéo sont disponibles, ainsi que pour le rendement pendant la capture en continu.</span><span class="sxs-lookup"><span data-stu-id="e2d92-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="e2d92-121">Les messages suivants définissent la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="e2d92-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="e2d92-122">Message</span><span class="sxs-lookup"><span data-stu-id="e2d92-122">Message</span></span>                                                                        | <span data-ttu-id="e2d92-123">Description</span><span class="sxs-lookup"><span data-stu-id="e2d92-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2d92-124">**WM \_ Cap \_ Set \_ callback \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="e2d92-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="e2d92-125">Spécifie la fonction de rappel dans l’application appelée pour fournir un contrôle précis sur le début et la fin de la capture.</span><span class="sxs-lookup"><span data-stu-id="e2d92-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="e2d92-126">Vous pouvez également utiliser la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="e2d92-127">**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2d92-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="e2d92-128">Spécifie la fonction de rappel dans l’application appelée lorsqu’une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e2d92-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="e2d92-129">Vous pouvez également utiliser la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="e2d92-130">**FRAME de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2d92-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="e2d92-131">Spécifie la fonction de rappel dans l’application appelée lorsque des frames d’aperçu sont capturés.</span><span class="sxs-lookup"><span data-stu-id="e2d92-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="e2d92-132">Vous pouvez également utiliser la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="e2d92-133">**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2d92-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="e2d92-134">Spécifie la fonction de rappel dans l’application appelée lorsque l’état change.</span><span class="sxs-lookup"><span data-stu-id="e2d92-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="e2d92-135">Vous pouvez également utiliser la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="e2d92-136">**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**</span><span class="sxs-lookup"><span data-stu-id="e2d92-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="e2d92-137">Spécifie la fonction de rappel dans l’application appelée pendant la capture en continu lorsqu’une nouvelle mémoire tampon vidéo est disponible.</span><span class="sxs-lookup"><span data-stu-id="e2d92-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="e2d92-138">Vous pouvez également utiliser la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="e2d92-139">**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**</span><span class="sxs-lookup"><span data-stu-id="e2d92-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="e2d92-140">Spécifie la fonction de rappel dans l’application appelée pendant la capture en continu lorsqu’une nouvelle mémoire tampon audio est disponible.</span><span class="sxs-lookup"><span data-stu-id="e2d92-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="e2d92-141">Vous pouvez également utiliser la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="e2d92-142">**\_jeu de \_ \_ rappels de la définition du jeu WM \_**</span><span class="sxs-lookup"><span data-stu-id="e2d92-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="e2d92-143">Spécifie la fonction de rappel dans l’application appelée lors de la création de la capture en continu.</span><span class="sxs-lookup"><span data-stu-id="e2d92-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="e2d92-144">Vous pouvez également utiliser la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) pour envoyer ce message.</span><span class="sxs-lookup"><span data-stu-id="e2d92-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="e2d92-145">Les rubriques suivantes décrivent les différentes fonctions de rappel, les notifications envoyées aux fonctions et leurs utilisations.</span><span class="sxs-lookup"><span data-stu-id="e2d92-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




