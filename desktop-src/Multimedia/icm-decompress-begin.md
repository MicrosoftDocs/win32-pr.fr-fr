---
title: Message ICM_DECOMPRESS_BEGIN (VFW. h)
description: Le message de début de décompression ICM \_ \_ envoie une notification à un pilote de décompression vidéo pour préparer la décompression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- Message ICM_DECOMPRESS_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105436"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="4dda5-105">Message de début de la \_ décompression ICM \_</span><span class="sxs-lookup"><span data-stu-id="4dda5-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="4dda5-106">Le message de **\_ \_ début** de décompression ICM envoie une notification à un pilote de décompression vidéo pour préparer la décompression des données.</span><span class="sxs-lookup"><span data-stu-id="4dda5-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="4dda5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="4dda5-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="4dda5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dda5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dda5-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="4dda5-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="4dda5-110">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4dda5-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="4dda5-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="4dda5-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="4dda5-112">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="4dda5-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dda5-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4dda5-113">Return Value</span></span>

<span data-ttu-id="4dda5-114">Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4dda5-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dda5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4dda5-115">Remarks</span></span>

<span data-ttu-id="4dda5-116">Lorsque le pilote reçoit ce message, il doit allouer des tampons et effectuer toutes les opérations qui prennent du temps afin qu’il puisse traiter les messages de [**\_ décompression ICM**](icm-decompress.md) de manière efficace.</span><span class="sxs-lookup"><span data-stu-id="4dda5-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="4dda5-117">Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message [**ICM \_ Draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="4dda5-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="4dda5-118">Les messages de [**\_ \_ fin**](icm-decompress-end.md) de décompression **ICM \_ \_ Begin** et ICM ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="4dda5-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="4dda5-119">Si le pilote reçoit la décompression ICM avant que la décompression ne soit arrêtée avec la **\_ \_ fin** de la décompression ICM, il doit redémarrer la décompression avec les nouveaux paramètres. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="4dda5-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dda5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dda5-120">Requirements</span></span>



| <span data-ttu-id="4dda5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dda5-121">Requirement</span></span> | <span data-ttu-id="4dda5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dda5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4dda5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dda5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4dda5-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dda5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4dda5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dda5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4dda5-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dda5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4dda5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dda5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dda5-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dda5-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dda5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4dda5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dda5-130">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="4dda5-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4dda5-131">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="4dda5-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

