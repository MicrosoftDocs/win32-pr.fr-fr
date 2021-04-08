---
title: Message ICM_DRAW_END (VFW. h)
description: Le \_ message ICM Draw \_ end indique à un pilote de rendu de décompresser l’image actuelle à l’écran et de libérer les ressources allouées pour la décompression et le dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- Message ICM_DRAW_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741964"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="9dd13-105">Message de fin de \_ dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="9dd13-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="9dd13-106">Le message **ICM \_ Draw \_ end** indique à un pilote de rendu de décompresser l’image actuelle à l’écran et de libérer les ressources allouées pour la décompression et le dessin.</span><span class="sxs-lookup"><span data-stu-id="9dd13-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="9dd13-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="9dd13-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="9dd13-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9dd13-108">Return Value</span></span>

<span data-ttu-id="9dd13-109">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9dd13-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd13-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9dd13-110">Remarks</span></span>

<span data-ttu-id="9dd13-111">Les messages de **\_ \_ fin** de dessin [**ICM \_ \_**](icm-draw-begin.md) et ICM ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="9dd13-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="9dd13-112">Si votre pilote reçoit **le \_ dessin \_ ICM, commencez** la décompression avec **les nouveaux paramètres \_ \_** pour arrêter la décompression.</span><span class="sxs-lookup"><span data-stu-id="9dd13-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd13-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dd13-113">Requirements</span></span>



| <span data-ttu-id="9dd13-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dd13-114">Requirement</span></span> | <span data-ttu-id="9dd13-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dd13-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9dd13-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dd13-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd13-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dd13-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9dd13-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dd13-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd13-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dd13-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9dd13-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dd13-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dd13-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd13-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd13-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dd13-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd13-123">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="9dd13-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="9dd13-124">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="9dd13-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





