---
title: Message ICM_DRAW (VFW. h)
description: Le \_ message ICM Draw notifie à un pilote de rendu de décompresser un frame de données et de le dessiner à l’écran.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- Message ICM_DRAW Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741172"
---
# <a name="icm_draw-message"></a><span data-ttu-id="84473-104">\_Message de dessin ICM</span><span class="sxs-lookup"><span data-stu-id="84473-104">ICM\_DRAW message</span></span>

<span data-ttu-id="84473-105">Le message **ICM \_ Draw** notifie à un pilote de rendu de décompresser un frame de données et de le dessiner à l’écran.</span><span class="sxs-lookup"><span data-stu-id="84473-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="84473-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84473-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84473-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="84473-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="84473-108">Pointeur vers une structure [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .</span><span class="sxs-lookup"><span data-stu-id="84473-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="84473-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="84473-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="84473-110">Taille, en octets, de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span><span class="sxs-lookup"><span data-stu-id="84473-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84473-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84473-111">Return Value</span></span>

<span data-ttu-id="84473-112">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84473-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84473-113">Notes</span><span class="sxs-lookup"><span data-stu-id="84473-113">Remarks</span></span>

<span data-ttu-id="84473-114">Si l' \_ indicateur de mise à jour ICDRAW est défini dans le membre **DwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), la zone de l’écran utilisée pour le dessin n’est pas valide et doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="84473-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="84473-115">L’étendue de la mise à jour dépend du contenu du membre **lpData** .</span><span class="sxs-lookup"><span data-stu-id="84473-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="84473-116">Si **lpData** a la **valeur null**, le pilote doit mettre à jour l’intégralité du rectangle de destination avec l’image actuelle.</span><span class="sxs-lookup"><span data-stu-id="84473-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="84473-117">Si le pilote conserve une copie de l’image dans une mémoire tampon hors écran, ce message peut échouer.</span><span class="sxs-lookup"><span data-stu-id="84473-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="84473-118">Si **lpData** n’a pas la **valeur null**, le pilote doit dessiner les données et vérifier que l’intégralité de la destination est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="84473-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="84473-119">Si l' \_ indicateur ICDRAW HURRYUP est défini dans **dwFlags**, l’application appelante souhaite que le pilote se poursuive le plus rapidement possible, sans doute même mettre à jour l’écran.</span><span class="sxs-lookup"><span data-stu-id="84473-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="84473-120">Si l' \_ indicateur de PRÉROLL ICDRAW est défini dans **dwFlags**, cette image vidéo est des informations préliminaires et ne doit pas être affichée si possible.</span><span class="sxs-lookup"><span data-stu-id="84473-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="84473-121">Par exemple, si la lecture doit commencer à partir de l’image 10, et que le frame 0 est l’image clé précédente la plus proche, les trames de 0 à 9 comportent le \_ PRÉROLL ICDRAW Set.</span><span class="sxs-lookup"><span data-stu-id="84473-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="84473-122">Si vous souhaitez que le pilote décompresse les données dans une mémoire tampon, envoyez le message de [**\_ décompression ICM**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="84473-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="84473-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84473-123">Requirements</span></span>



| <span data-ttu-id="84473-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84473-124">Requirement</span></span> | <span data-ttu-id="84473-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="84473-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84473-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84473-126">Minimum supported client</span></span><br/> | <span data-ttu-id="84473-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84473-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84473-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84473-128">Minimum supported server</span></span><br/> | <span data-ttu-id="84473-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84473-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84473-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="84473-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="84473-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="84473-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84473-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84473-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84473-133">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="84473-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="84473-134">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="84473-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





