---
title: Message ICM_COMPRESS_GET_FORMAT (VFW. h)
description: Le \_ \_ \_ message de format d’extraction de la compression ICM demande le format de sortie des données compressées à partir d’un pilote de compression vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- Message ICM_COMPRESS_GET_FORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466475"
---
# <a name="icm_compress_get_format-message"></a><span data-ttu-id="00f0a-105">\_Message de \_ format d’extraction de la compression ICM \_</span><span class="sxs-lookup"><span data-stu-id="00f0a-105">ICM\_COMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="00f0a-106">Le message de format d’extraction de la **\_ compression \_ \_ ICM** demande le format de sortie des données compressées à partir d’un pilote de compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="00f0a-106">The **ICM\_COMPRESS\_GET\_FORMAT** message requests the output format of the compressed data from a video compression driver.</span></span> <span data-ttu-id="00f0a-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="00f0a-107">You can send this message explicitly or by using the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro.</span></span>


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="00f0a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00f0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f0a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="00f0a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="00f0a-110">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="00f0a-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="00f0a-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="00f0a-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="00f0a-112">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) pour contenir le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="00f0a-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="00f0a-113">Vous pouvez spécifier zéro pour ce paramètre pour demander uniquement la taille du format de sortie, comme dans la macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="00f0a-113">You can specify zero for this parameter to request only the size of the output format, as in the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f0a-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00f0a-114">Return Value</span></span>

<span data-ttu-id="00f0a-115">Si *lpbiOutput* est égal à zéro, retourne la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="00f0a-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="00f0a-116">Si *lpbiOutput* est différent de zéro, retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="00f0a-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00f0a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="00f0a-117">Remarks</span></span>

<span data-ttu-id="00f0a-118">Si *lpbiOutput* est différent de zéro, le pilote doit remplir la structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) avec le format de sortie par défaut correspondant au format d’entrée spécifié pour *lpbiInput*.</span><span class="sxs-lookup"><span data-stu-id="00f0a-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="00f0a-119">Si le compresseur peut produire plusieurs formats, le format par défaut doit être celui qui conserve la plus grande quantité d’informations.</span><span class="sxs-lookup"><span data-stu-id="00f0a-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="00f0a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00f0a-120">Requirements</span></span>



| <span data-ttu-id="00f0a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00f0a-121">Requirement</span></span> | <span data-ttu-id="00f0a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="00f0a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="00f0a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00f0a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="00f0a-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00f0a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="00f0a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00f0a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="00f0a-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00f0a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="00f0a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="00f0a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f0a-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f0a-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00f0a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00f0a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00f0a-130">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="00f0a-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="00f0a-131">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="00f0a-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

