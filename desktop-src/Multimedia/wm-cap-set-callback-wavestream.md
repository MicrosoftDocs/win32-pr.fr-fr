---
title: Message WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: Le \_ message de \_ rappel de la valeur du paramètre WM Cap Set \_ \_ définit une fonction de rappel dans l’application.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- Message WM_CAP_SET_CALLBACK_WAVESTREAM Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466867"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="bb6d8-104">\_ \_ \_ Message WAVESTREAM de rappel \_ défini par WM Cap</span><span class="sxs-lookup"><span data-stu-id="bb6d8-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="bb6d8-105">Le message de rappel de la **\_ valeur du paramètre WM Cap \_ Set \_ \_** définit une fonction de rappel dans l’application.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="bb6d8-106">AVICap appelle cette procédure lors de la capture en continu lorsqu’une nouvelle mémoire tampon audio est disponible.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="bb6d8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .</span><span class="sxs-lookup"><span data-stu-id="bb6d8-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="bb6d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb6d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb6d8-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="bb6d8-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="bb6d8-110">Pointeur vers la fonction de rappel de flux Wave, de type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span><span class="sxs-lookup"><span data-stu-id="bb6d8-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="bb6d8-111">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel de flux Wave précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb6d8-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb6d8-112">Return Value</span></span>

<span data-ttu-id="bb6d8-113">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb6d8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bb6d8-114">Remarks</span></span>

<span data-ttu-id="bb6d8-115">La fenêtre de capture appelle la procédure avant d’écrire la mémoire tampon audio sur le disque.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="bb6d8-116">Cela permet aux applications de modifier la mémoire tampon audio si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="bb6d8-117">Si une fonction de rappel de flux Wave est utilisée, elle doit être installée avant le démarrage de la session de capture et elle doit rester activée pendant toute la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="bb6d8-118">Elle peut être désactivée après la fin de la capture de streaming.</span><span class="sxs-lookup"><span data-stu-id="bb6d8-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6d8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb6d8-119">Requirements</span></span>



| <span data-ttu-id="bb6d8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb6d8-120">Requirement</span></span> | <span data-ttu-id="bb6d8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb6d8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bb6d8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb6d8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6d8-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb6d8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bb6d8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb6d8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6d8-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb6d8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bb6d8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb6d8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb6d8-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d8-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6d8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb6d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6d8-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="bb6d8-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bb6d8-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="bb6d8-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





