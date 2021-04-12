---
title: Message ICM_DRAW_START (VFW. h)
description: Le \_ message de début de dessin ICM \_ indique à un pilote de rendu de démarrer son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- Message ICM_DRAW_START Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384483"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="58172-105">Message de début de \_ dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="58172-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="58172-106">Le message de **\_ \_ début de dessin ICM** indique à un pilote de rendu de démarrer son horloge interne pour le minutage des frames de dessin.</span><span class="sxs-lookup"><span data-stu-id="58172-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="58172-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .</span><span class="sxs-lookup"><span data-stu-id="58172-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="58172-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58172-108">Return Value</span></span>

<span data-ttu-id="58172-109">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="58172-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58172-110">Notes</span><span class="sxs-lookup"><span data-stu-id="58172-110">Remarks</span></span>

<span data-ttu-id="58172-111">Ce message est utilisé par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.</span><span class="sxs-lookup"><span data-stu-id="58172-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="58172-112">Lorsque le pilote reçoit ce message, il doit commencer à afficher les données à la fréquence spécifiée avec le message de [**\_ \_ début**](icm-draw-begin.md) de l’ICM.</span><span class="sxs-lookup"><span data-stu-id="58172-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="58172-113">Les messages d' [**\_ \_ arrêt**](icm-draw-stop.md) de dessin **ICM \_ \_** et ICM ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="58172-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="58172-114">Si votre pilote reçoit **le \_ dessin \_ ICM, démarrer** avant l’arrêt du rendu avec **ICM \_ Draw \_ Stop**, il doit redémarrer le rendu avec de nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="58172-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="58172-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58172-115">Requirements</span></span>



| <span data-ttu-id="58172-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58172-116">Requirement</span></span> | <span data-ttu-id="58172-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="58172-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="58172-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58172-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58172-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58172-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="58172-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58172-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58172-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58172-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58172-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="58172-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58172-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="58172-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58172-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58172-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58172-125">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="58172-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="58172-126">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="58172-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





