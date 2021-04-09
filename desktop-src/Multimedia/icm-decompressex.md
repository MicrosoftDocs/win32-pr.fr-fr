---
title: Message ICM_DECOMPRESSEX (VFW. h)
description: Le \_ message DECOMPRESSEX ICM indique à un pilote de compression vidéo de décompresser un frame de données directement à l’écran, d’effectuer une décompression vers un DIB inversé ou de décompresser des images décrites dans des rectangles source et de destination.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- Message ICM_DECOMPRESSEX Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033129"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="f3617-104">\_Message DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="f3617-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="f3617-105">Le **message \_ DECOMPRESSEX ICM** indique à un pilote de compression vidéo de décompresser un frame de données directement à l’écran, d’effectuer une décompression vers un DIB inversé ou de décompresser des images décrites dans des rectangles source et de destination.</span><span class="sxs-lookup"><span data-stu-id="f3617-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="f3617-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3617-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3617-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="f3617-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="f3617-108">Pointeur vers une structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .</span><span class="sxs-lookup"><span data-stu-id="f3617-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3617-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3617-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f3617-110">Taille, en octets, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="f3617-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3617-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f3617-111">Return Value</span></span>

<span data-ttu-id="f3617-112">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f3617-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3617-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f3617-113">Remarks</span></span>

<span data-ttu-id="f3617-114">Ce message est similaire à [**la \_ décompression ICM**](icm-decompress.md) , sauf qu’elle utilise la structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) pour définir ses informations de décompression.</span><span class="sxs-lookup"><span data-stu-id="f3617-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="f3617-115">Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message [**ICM \_ Draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="f3617-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="f3617-116">Le pilote retourne une erreur si ce message est reçu avant le message de [**\_ \_ début de DECOMPRESSEX ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="f3617-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3617-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3617-117">Requirements</span></span>



| <span data-ttu-id="f3617-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3617-118">Requirement</span></span> | <span data-ttu-id="f3617-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3617-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3617-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3617-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3617-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3617-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3617-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3617-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3617-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3617-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3617-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3617-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3617-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3617-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3617-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3617-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3617-127">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="f3617-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f3617-128">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="f3617-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





