---
title: Message WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ yield définit une fonction de rappel dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture est obtenue pendant la capture en continu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- Message WM_CAP_SET_CALLBACK_YIELD Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511925"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="6a66c-106">\_Message de \_ \_ \_ régénérer le rappel de la définition de l’embout WM</span><span class="sxs-lookup"><span data-stu-id="6a66c-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="6a66c-107">Le message **WM \_ Cap \_ Set \_ callback \_ yield** définit une fonction de rappel dans l’application.</span><span class="sxs-lookup"><span data-stu-id="6a66c-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="6a66c-108">AVICap appelle cette procédure lorsque la fenêtre de capture est obtenue pendant la capture en continu.</span><span class="sxs-lookup"><span data-stu-id="6a66c-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="6a66c-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .</span><span class="sxs-lookup"><span data-stu-id="6a66c-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="6a66c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a66c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a66c-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="6a66c-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="6a66c-112">Pointeur vers la fonction de rappel yield, de type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span><span class="sxs-lookup"><span data-stu-id="6a66c-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="6a66c-113">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel yield précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="6a66c-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a66c-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a66c-114">Return Value</span></span>

<span data-ttu-id="6a66c-115">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="6a66c-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a66c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6a66c-116">Remarks</span></span>

<span data-ttu-id="6a66c-117">Les applications peuvent éventuellement définir une fonction de rappel yield.</span><span class="sxs-lookup"><span data-stu-id="6a66c-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="6a66c-118">La fonction de rappel Yield est appelée au moins une fois pour chaque image vidéo capturée pendant la capture en continu.</span><span class="sxs-lookup"><span data-stu-id="6a66c-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="6a66c-119">Si une fonction de rappel Yield est installée, elle est appelée indépendamment de l’état du membre **fYield** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="6a66c-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="6a66c-120">Si la fonction de rappel Yield est utilisée, elle doit être installée avant le démarrage de la session de capture et elle doit rester activée pendant toute la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="6a66c-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="6a66c-121">Elle peut être désactivée après la fin de la capture de streaming.</span><span class="sxs-lookup"><span data-stu-id="6a66c-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="6a66c-122">Les applications exécutent généralement un certain type de traitement des messages dans la fonction de rappel composée d’une boucle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , comme dans la boucle de message d’une fonction [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="6a66c-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="6a66c-123">La fonction de rappel yield doit également filtrer et supprimer les messages qui peuvent provoquer des problèmes de réentrance.</span><span class="sxs-lookup"><span data-stu-id="6a66c-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="6a66c-124">Une application retourne généralement la **valeur true** dans la procédure yield pour continuer la capture de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="6a66c-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="6a66c-125">Si une fonction de rappel yield retourne la **valeur false**, la fenêtre de capture arrête le processus de capture.</span><span class="sxs-lookup"><span data-stu-id="6a66c-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a66c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a66c-126">Requirements</span></span>



| <span data-ttu-id="6a66c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a66c-127">Requirement</span></span> | <span data-ttu-id="6a66c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a66c-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6a66c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a66c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a66c-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a66c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6a66c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a66c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a66c-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a66c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a66c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a66c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a66c-134"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a66c-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a66c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a66c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a66c-136">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="6a66c-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6a66c-137">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="6a66c-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

