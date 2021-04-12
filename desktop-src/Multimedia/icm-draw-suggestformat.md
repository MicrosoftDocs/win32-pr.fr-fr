---
title: Message ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: Le \_ message SUGGESTFORMAT de dessin ICM \_ interroge un pilote de rendu pour suggérer un format décompressé qu’il peut dessiner.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- Message ICM_DRAW_SUGGESTFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464631"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="95c47-104">\_Message SUGGESTFORMAT de dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="95c47-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="95c47-105">Le **message \_ \_ SUGGESTFORMAT de dessin ICM** interroge un pilote de rendu pour suggérer un format décompressé qu’il peut dessiner.</span><span class="sxs-lookup"><span data-stu-id="95c47-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="95c47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95c47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c47-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span><span class="sxs-lookup"><span data-stu-id="95c47-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="95c47-108">Pointeur vers une structure [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .</span><span class="sxs-lookup"><span data-stu-id="95c47-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="95c47-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="95c47-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="95c47-110">Taille, en octets, de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span><span class="sxs-lookup"><span data-stu-id="95c47-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c47-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="95c47-111">Return Value</span></span>

<span data-ttu-id="95c47-112">Retourne ICERR \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="95c47-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="95c47-113">Si le membre **lpbiSuggest** de la structure [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) est **null**, ce message retourne la quantité de mémoire nécessaire pour contenir le format suggéré.</span><span class="sxs-lookup"><span data-stu-id="95c47-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="95c47-114">Notes</span><span class="sxs-lookup"><span data-stu-id="95c47-114">Remarks</span></span>

<span data-ttu-id="95c47-115">Le pilote doit examiner le format spécifié dans le membre **lpbiIn** de la structure [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) et utiliser le membre **lpbiSuggest** pour retourner un format qu’il peut dessiner.</span><span class="sxs-lookup"><span data-stu-id="95c47-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="95c47-116">Le format de sortie doit conserver autant de données que possible à partir du format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="95c47-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="95c47-117">Le cas échéant, le pilote peut utiliser le descripteur de compresseur installable passé dans le membre **hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) pour effectuer des sélections plus complexes.</span><span class="sxs-lookup"><span data-stu-id="95c47-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="95c47-118">Par exemple, si le format d’entrée est données JPEG de 24 bits, un convertisseur peut interroger le décompresseur pour déterminer s’il peut être décompressé dans un format YUV (qui peut être dessiné plus efficacement) avant de sélectionner le format à suggérer.</span><span class="sxs-lookup"><span data-stu-id="95c47-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c47-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95c47-119">Requirements</span></span>



| <span data-ttu-id="95c47-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95c47-120">Requirement</span></span> | <span data-ttu-id="95c47-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="95c47-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="95c47-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95c47-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95c47-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95c47-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="95c47-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95c47-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95c47-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95c47-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95c47-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="95c47-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c47-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c47-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c47-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95c47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c47-129">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="95c47-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="95c47-130">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="95c47-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





