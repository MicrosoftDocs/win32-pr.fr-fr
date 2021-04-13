---
title: Message ICM_DRAW_WINDOW (VFW. h)
description: Le \_ message de fenêtre de dessin ICM \_ indique à un pilote de rendu que la fenêtre spécifiée pour le \_ message de début du dessin ICM \_ doit être redessinée.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- Message ICM_DRAW_WINDOW Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464991"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="df6cb-104">Message de fenêtre de \_ dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="df6cb-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="df6cb-105">Le message de **\_ \_ fenêtre de dessin ICM** indique à un pilote de rendu que la fenêtre spécifiée pour le message de [**\_ \_ début du dessin ICM**](icm-draw-begin.md) doit être redessinée.</span><span class="sxs-lookup"><span data-stu-id="df6cb-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="df6cb-106">La fenêtre a été déplacée ou devenue temporairement masquée.</span><span class="sxs-lookup"><span data-stu-id="df6cb-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="df6cb-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .</span><span class="sxs-lookup"><span data-stu-id="df6cb-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="df6cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df6cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6cb-109"><span id="prc"></span><span id="PRC"></span>*République*</span><span class="sxs-lookup"><span data-stu-id="df6cb-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="df6cb-110">Pointeur vers le rectangle de destination en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="df6cb-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="df6cb-111">Si ce paramètre pointe vers un rectangle vide, le dessin doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="df6cb-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6cb-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df6cb-112">Return Value</span></span>

<span data-ttu-id="df6cb-113">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="df6cb-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df6cb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="df6cb-114">Remarks</span></span>

<span data-ttu-id="df6cb-115">Ce message est pris en charge par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.</span><span class="sxs-lookup"><span data-stu-id="df6cb-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="df6cb-116">Les pilotes vidéo-superposition utilisent ce message pour dessiner lorsque la fenêtre est masquée ou déplacée.</span><span class="sxs-lookup"><span data-stu-id="df6cb-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="df6cb-117">Quand une fenêtre spécifiée pour [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) est complètement masquée par d’autres fenêtres, le rectangle de destination est vide.</span><span class="sxs-lookup"><span data-stu-id="df6cb-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="df6cb-118">Les pilotes doivent désactiver le matériel de superposition vidéo lorsque cette condition se produit.</span><span class="sxs-lookup"><span data-stu-id="df6cb-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6cb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df6cb-119">Requirements</span></span>



| <span data-ttu-id="df6cb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df6cb-120">Requirement</span></span> | <span data-ttu-id="df6cb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="df6cb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df6cb-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df6cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df6cb-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df6cb-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df6cb-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df6cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df6cb-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df6cb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df6cb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="df6cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df6cb-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6cb-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6cb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df6cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6cb-129">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="df6cb-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="df6cb-130">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="df6cb-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





