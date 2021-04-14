---
title: Message WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ VIDEOSTREAM définit une fonction de rappel dans l’application.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- Message WM_CAP_SET_CALLBACK_VIDEOSTREAM Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383923"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="965e3-104">\_ \_ \_ Message VIDEOSTREAM de rappel Set callback \_ de WM</span><span class="sxs-lookup"><span data-stu-id="965e3-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="965e3-105">Le message **WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM** définit une fonction de rappel dans l’application.</span><span class="sxs-lookup"><span data-stu-id="965e3-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="965e3-106">AVICap appelle cette procédure lors de la capture en continu lorsqu’une mémoire tampon vidéo est remplie.</span><span class="sxs-lookup"><span data-stu-id="965e3-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="965e3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .</span><span class="sxs-lookup"><span data-stu-id="965e3-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="965e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="965e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965e3-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="965e3-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="965e3-110">Pointeur vers la fonction de rappel de flux vidéo, de type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="965e3-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="965e3-111">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel de flux vidéo précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="965e3-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965e3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="965e3-112">Return Value</span></span>

<span data-ttu-id="965e3-113">Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="965e3-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="965e3-114">Notes</span><span class="sxs-lookup"><span data-stu-id="965e3-114">Remarks</span></span>

<span data-ttu-id="965e3-115">La fenêtre de capture appelle la fonction de rappel avant d’écrire le frame capturé sur le disque.</span><span class="sxs-lookup"><span data-stu-id="965e3-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="965e3-116">Cela permet aux applications de modifier le frame si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="965e3-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="965e3-117">Si une fonction de rappel de flux vidéo est utilisée pour la capture en continu, la procédure doit être installée avant le démarrage de la session de capture et elle doit rester activée pendant toute la durée de la session.</span><span class="sxs-lookup"><span data-stu-id="965e3-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="965e3-118">Elle peut être désactivée après la fin de la capture de streaming.</span><span class="sxs-lookup"><span data-stu-id="965e3-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="965e3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="965e3-119">Requirements</span></span>



| <span data-ttu-id="965e3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="965e3-120">Requirement</span></span> | <span data-ttu-id="965e3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="965e3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="965e3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="965e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="965e3-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="965e3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="965e3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="965e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="965e3-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="965e3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="965e3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="965e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="965e3-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="965e3-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965e3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="965e3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965e3-129">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="965e3-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="965e3-130">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="965e3-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





