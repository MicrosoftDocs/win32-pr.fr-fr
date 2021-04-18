---
title: Message WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ CAPCONTROL définit une fonction de rappel dans l’application, ce qui lui donne un contrôle d’enregistrement précis. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- Message WM_CAP_SET_CALLBACK_CAPCONTROL Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512167"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="438e8-105">\_ \_ \_ Message CAPCONTROL de rappel Set callback \_ de WM</span><span class="sxs-lookup"><span data-stu-id="438e8-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="438e8-106">Le message **WM \_ Cap \_ Set \_ callback \_ CAPCONTROL** définit une fonction de rappel dans l’application, ce qui lui donne un contrôle d’enregistrement précis.</span><span class="sxs-lookup"><span data-stu-id="438e8-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="438e8-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .</span><span class="sxs-lookup"><span data-stu-id="438e8-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="438e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="438e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="438e8-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="438e8-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="438e8-110">Pointeur vers la fonction de rappel, de type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span><span class="sxs-lookup"><span data-stu-id="438e8-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="438e8-111">Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel précédemment installée.</span><span class="sxs-lookup"><span data-stu-id="438e8-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="438e8-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="438e8-112">Return Value</span></span>

<span data-ttu-id="438e8-113">Retourne la **valeur true** en cas de réussite ou **false** si une capture de streaming ou une session de capture de trame unique est en cours.</span><span class="sxs-lookup"><span data-stu-id="438e8-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="438e8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="438e8-114">Remarks</span></span>

<span data-ttu-id="438e8-115">Une fonction de rappel unique est utilisée pour permettre à l’application de contrôler précisément le moment où la capture de la diffusion en continu commence et se termine.</span><span class="sxs-lookup"><span data-stu-id="438e8-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="438e8-116">La fenêtre de capture appelle d’abord la procédure avec *nState* défini sur le \_ préroll CONTROLCALLBACK une fois que toutes les mémoires tampons ont été allouées et que toutes les autres préparations de capture sont terminées.</span><span class="sxs-lookup"><span data-stu-id="438e8-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="438e8-117">Cela donne à l’application la possibilité de Prérouler des sources vidéo, en retournant à partir de la fonction de rappel à l’enregistrement exact du moment.</span><span class="sxs-lookup"><span data-stu-id="438e8-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="438e8-118">La valeur de retour **true** de la fonction de rappel continue la capture et la valeur de retour **false** abandonne la capture.</span><span class="sxs-lookup"><span data-stu-id="438e8-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="438e8-119">Une fois la capture commencée, cette fonction de rappel est appelée fréquemment avec *nState* défini sur la \_ capture CONTROLCALLBACK pour permettre à l’application de terminer la capture en renvoyant **false**.</span><span class="sxs-lookup"><span data-stu-id="438e8-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="438e8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="438e8-120">Requirements</span></span>



| <span data-ttu-id="438e8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="438e8-121">Requirement</span></span> | <span data-ttu-id="438e8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="438e8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="438e8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="438e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="438e8-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="438e8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="438e8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="438e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="438e8-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="438e8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="438e8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="438e8-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="438e8-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="438e8-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="438e8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="438e8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="438e8-130">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="438e8-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="438e8-131">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="438e8-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





