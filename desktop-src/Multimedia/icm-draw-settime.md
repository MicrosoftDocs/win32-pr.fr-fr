---
title: Message ICM_DRAW_SETTIME (VFW. h)
description: La \_ commande ICM Draw \_ setTime fournit des informations de synchronisation à un pilote de rendu qui gère le minutage des frames de dessin.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- Message ICM_DRAW_SETTIME Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843405"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="07850-104">\_Message de dessin de ICM ICM \_</span><span class="sxs-lookup"><span data-stu-id="07850-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="07850-105">La commande **ICM \_ Draw \_ setTime** fournit des informations de synchronisation à un pilote de rendu qui gère le minutage des frames de dessin.</span><span class="sxs-lookup"><span data-stu-id="07850-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="07850-106">Les informations de synchronisation sont le numéro d’exemple du cadre à dessiner.</span><span class="sxs-lookup"><span data-stu-id="07850-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="07850-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .</span><span class="sxs-lookup"><span data-stu-id="07850-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="07850-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07850-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07850-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span><span class="sxs-lookup"><span data-stu-id="07850-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="07850-110">Exemple de numéro de l’image à afficher.</span><span class="sxs-lookup"><span data-stu-id="07850-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07850-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07850-111">Return Value</span></span>

<span data-ttu-id="07850-112">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="07850-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07850-113">Notes</span><span class="sxs-lookup"><span data-stu-id="07850-113">Remarks</span></span>

<span data-ttu-id="07850-114">En général, le pilote compare la valeur spécifiée avec le numéro de frame associé à l’heure de son horloge interne et tente de synchroniser les deux si la différence est importante.</span><span class="sxs-lookup"><span data-stu-id="07850-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="07850-115">Utilisez ce message lorsque le matériel effectue sa propre décompression, synchronisation et dessin asynchrones, et que le matériel s’appuie sur un signal de synchronisation externe (le matériel n’est pas utilisé en tant que maître de synchronisation).</span><span class="sxs-lookup"><span data-stu-id="07850-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="07850-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07850-116">Requirements</span></span>



| <span data-ttu-id="07850-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07850-117">Requirement</span></span> | <span data-ttu-id="07850-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="07850-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="07850-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07850-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07850-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07850-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="07850-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07850-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07850-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07850-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="07850-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="07850-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="07850-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="07850-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07850-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07850-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07850-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="07850-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="07850-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="07850-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





