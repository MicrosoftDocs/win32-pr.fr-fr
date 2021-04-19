---
title: Message ICM_DRAW_GETTIME (VFW. h)
description: Le \_ message ICM Draw \_ GETTIME demande un pilote de rendu qui contrôle le minutage des frames de dessin pour retourner la valeur actuelle de son horloge interne. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawGetTime.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- Message ICM_DRAW_GETTIME Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511571"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="aa073-105">\_Message de \_ cogettime de dessin ICM</span><span class="sxs-lookup"><span data-stu-id="aa073-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="aa073-106">Le message **ICM \_ Draw \_ GETTIME** demande un pilote de rendu qui contrôle le minutage des frames de dessin pour retourner la valeur actuelle de son horloge interne.</span><span class="sxs-lookup"><span data-stu-id="aa073-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="aa073-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) .</span><span class="sxs-lookup"><span data-stu-id="aa073-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="aa073-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa073-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span><span class="sxs-lookup"><span data-stu-id="aa073-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="aa073-110">Adresse qui doit contenir l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="aa073-110">Address to contain the current time.</span></span> <span data-ttu-id="aa073-111">La valeur de retour doit être spécifiée dans des exemples.</span><span class="sxs-lookup"><span data-stu-id="aa073-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa073-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aa073-112">Return Value</span></span>

<span data-ttu-id="aa073-113">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="aa073-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa073-114">Notes</span><span class="sxs-lookup"><span data-stu-id="aa073-114">Remarks</span></span>

<span data-ttu-id="aa073-115">Ce message est généralement pris en charge par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.</span><span class="sxs-lookup"><span data-stu-id="aa073-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="aa073-116">Le message peut également être envoyé si le matériel est utilisé en tant que maître de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="aa073-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa073-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa073-117">Requirements</span></span>



| <span data-ttu-id="aa073-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa073-118">Requirement</span></span> | <span data-ttu-id="aa073-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa073-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="aa073-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa073-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa073-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa073-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="aa073-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa073-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa073-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa073-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aa073-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa073-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa073-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa073-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa073-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa073-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa073-127">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="aa073-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="aa073-128">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="aa073-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





