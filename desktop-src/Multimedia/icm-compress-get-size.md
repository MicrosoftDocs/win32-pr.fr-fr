---
title: Message ICM_COMPRESS_GET_SIZE (VFW. h)
description: Le message de taille de la \_ compression ICM \_ \_ demande que le pilote de compression vidéo fournisse la taille maximale d’une trame de données lorsqu’elle est compressée dans le format de sortie spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- Message ICM_COMPRESS_GET_SIZE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942634"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="76220-105">Message de taille de la \_ compression ICM \_ \_</span><span class="sxs-lookup"><span data-stu-id="76220-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="76220-106">Le message de **\_ \_ \_ taille de la compression ICM** demande que le pilote de compression vidéo fournisse la taille maximale d’une trame de données lorsqu’elle est compressée dans le format de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="76220-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="76220-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .</span><span class="sxs-lookup"><span data-stu-id="76220-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="76220-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76220-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76220-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="76220-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="76220-110">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="76220-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="76220-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="76220-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="76220-112">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="76220-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76220-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="76220-113">Return Value</span></span>

<span data-ttu-id="76220-114">Retourne le nombre maximal d’octets qu’un seul Frame compressé peut occuper.</span><span class="sxs-lookup"><span data-stu-id="76220-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="76220-115">Notes</span><span class="sxs-lookup"><span data-stu-id="76220-115">Remarks</span></span>

<span data-ttu-id="76220-116">En règle générale, les applications envoient ce message pour déterminer la taille d’une mémoire tampon à allouer pour le frame compressé.</span><span class="sxs-lookup"><span data-stu-id="76220-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="76220-117">Le pilote doit calculer la taille du plus grand Frame possible en fonction des formats d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="76220-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="76220-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76220-118">Requirements</span></span>



| <span data-ttu-id="76220-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76220-119">Requirement</span></span> | <span data-ttu-id="76220-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="76220-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="76220-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76220-121">Minimum supported client</span></span><br/> | <span data-ttu-id="76220-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76220-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="76220-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76220-123">Minimum supported server</span></span><br/> | <span data-ttu-id="76220-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76220-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="76220-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="76220-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="76220-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="76220-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76220-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76220-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76220-128">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="76220-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="76220-129">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="76220-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

