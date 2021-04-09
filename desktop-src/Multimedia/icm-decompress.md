---
title: Message ICM_DECOMPRESS (VFW. h)
description: Le \_ message de décompression ICM indique à un pilote de décompression vidéo de décompresser une trame de données dans une mémoire tampon définie par l’application.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- Message ICM_DECOMPRESS Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033130"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="eab2d-104">\_Message de décompression ICM</span><span class="sxs-lookup"><span data-stu-id="eab2d-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="eab2d-105">Le message de décompression **ICM \_** indique à un pilote de décompression vidéo de décompresser une trame de données dans une mémoire tampon définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="eab2d-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="eab2d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eab2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab2d-107"><span id="icd"></span><span id="ICD"></span>*ICD*</span><span class="sxs-lookup"><span data-stu-id="eab2d-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="eab2d-108">Pointeur vers une structure [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .</span><span class="sxs-lookup"><span data-stu-id="eab2d-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="eab2d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="eab2d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="eab2d-110">Taille, en octets, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span><span class="sxs-lookup"><span data-stu-id="eab2d-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab2d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eab2d-111">Return Value</span></span>

<span data-ttu-id="eab2d-112">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="eab2d-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab2d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eab2d-113">Remarks</span></span>

<span data-ttu-id="eab2d-114">Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message [**ICM \_ Draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="eab2d-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="eab2d-115">Le pilote renvoie une erreur si ce message est reçu avant le message de début de la [**\_ \_ décompression ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="eab2d-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab2d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eab2d-116">Requirements</span></span>



| <span data-ttu-id="eab2d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eab2d-117">Requirement</span></span> | <span data-ttu-id="eab2d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="eab2d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eab2d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eab2d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eab2d-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eab2d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eab2d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eab2d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eab2d-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eab2d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eab2d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="eab2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eab2d-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab2d-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab2d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eab2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab2d-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="eab2d-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="eab2d-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="eab2d-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





