---
title: Message WM_CAP_SEQUENCE (VFW. h)
description: Le message de séquence de l' \_ embout WM \_ initie la diffusion vidéo et la capture audio dans un fichier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- Message WM_CAP_SEQUENCE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942271"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="ac19c-105">Message de séquence de l' \_ embout WM \_</span><span class="sxs-lookup"><span data-stu-id="ac19c-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="ac19c-106">Le message de **\_ \_ séquence de l’embout WM** initie la diffusion vidéo et la capture audio dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ac19c-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="ac19c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .</span><span class="sxs-lookup"><span data-stu-id="ac19c-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="ac19c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ac19c-108">Return Value</span></span>

<span data-ttu-id="ac19c-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ac19c-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="ac19c-110">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="ac19c-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac19c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ac19c-111">Remarks</span></span>

<span data-ttu-id="ac19c-112">Si vous souhaitez modifier les paramètres de contrôle de la capture en continu, utilisez le message [**\_ \_ \_ \_ d’installation de la séquence WM Cap Set**](wm-cap-set-sequence-setup.md) avant de démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="ac19c-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="ac19c-113">Par défaut, la fenêtre de capture ne permet pas à d’autres applications de continuer à s’exécuter pendant la capture.</span><span class="sxs-lookup"><span data-stu-id="ac19c-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="ac19c-114">Pour remplacer cette valeur, affectez la **valeur true** au membre **fYield** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) ou installez une fonction de rappel yield.</span><span class="sxs-lookup"><span data-stu-id="ac19c-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="ac19c-115">Pendant la capture en continu, la fenêtre de capture peut éventuellement émettre des notifications pour votre application de types spécifiques de conditions.</span><span class="sxs-lookup"><span data-stu-id="ac19c-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="ac19c-116">Pour installer des procédures de rappel pour ces notifications, utilisez les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="ac19c-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="ac19c-117">**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ac19c-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="ac19c-118">**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ac19c-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="ac19c-119">**\_jeu de \_ \_ rappels de la définition du jeu WM \_**</span><span class="sxs-lookup"><span data-stu-id="ac19c-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="ac19c-120">**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**</span><span class="sxs-lookup"><span data-stu-id="ac19c-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="ac19c-121">**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**</span><span class="sxs-lookup"><span data-stu-id="ac19c-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="ac19c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac19c-122">Requirements</span></span>



| <span data-ttu-id="ac19c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac19c-123">Requirement</span></span> | <span data-ttu-id="ac19c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac19c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac19c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac19c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ac19c-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac19c-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac19c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac19c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ac19c-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac19c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac19c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac19c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac19c-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac19c-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac19c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac19c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac19c-132">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="ac19c-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ac19c-133">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="ac19c-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





