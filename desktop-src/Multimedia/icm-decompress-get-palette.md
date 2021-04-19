---
title: Message ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: Le \_ \_ message d’extraction de la palette ICM décompresse les \_ demandes que le pilote de décompression vidéo fournisse la table des couleurs de la structure BITMAPINFOHEADER de sortie. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- Message ICM_DECOMPRESS_GET_PALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510560"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="84290-105">Message d’extraction de la \_ \_ \_ palette ICM</span><span class="sxs-lookup"><span data-stu-id="84290-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="84290-106">Le message d’extraction de la **\_ \_ \_ palette ICM décompresse** les demandes que le pilote de décompression vidéo fournisse la table des couleurs de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) de sortie.</span><span class="sxs-lookup"><span data-stu-id="84290-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="84290-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="84290-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="84290-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84290-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84290-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="84290-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="84290-110">Pointeur vers une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="84290-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="84290-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="84290-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="84290-112">Pointeur vers une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) pour contenir la table de couleurs.</span><span class="sxs-lookup"><span data-stu-id="84290-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="84290-113">L’espace réservé pour la table de couleurs est toujours au moins de 256 couleurs.</span><span class="sxs-lookup"><span data-stu-id="84290-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="84290-114">Vous pouvez spécifier zéro pour ce paramètre pour retourner uniquement la taille de la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="84290-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84290-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="84290-115">Return Value</span></span>

<span data-ttu-id="84290-116">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="84290-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84290-117">Notes</span><span class="sxs-lookup"><span data-stu-id="84290-117">Remarks</span></span>

<span data-ttu-id="84290-118">Si *lpbiOutput* est différent de zéro, le pilote définit le membre **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) sur le nombre de couleurs dans la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="84290-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="84290-119">Le pilote remplit le membre **bmiColors** de [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) avec les couleurs réelles.</span><span class="sxs-lookup"><span data-stu-id="84290-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="84290-120">Le pilote ne doit prendre en charge ce message que s’il utilise une palette différente de celle spécifiée dans le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="84290-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="84290-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84290-121">Requirements</span></span>



| <span data-ttu-id="84290-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84290-122">Requirement</span></span> | <span data-ttu-id="84290-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="84290-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="84290-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84290-124">Minimum supported client</span></span><br/> | <span data-ttu-id="84290-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84290-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="84290-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84290-126">Minimum supported server</span></span><br/> | <span data-ttu-id="84290-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84290-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84290-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="84290-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="84290-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="84290-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84290-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84290-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84290-131">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="84290-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="84290-132">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="84290-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

