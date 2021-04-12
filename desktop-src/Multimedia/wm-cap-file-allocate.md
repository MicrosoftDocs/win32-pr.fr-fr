---
title: Message WM_CAP_FILE_ALLOCATE (VFW. h)
description: Le \_ message WM \_ Cap \_ allocate crée (Préalloue) un fichier de capture d’une taille spécifiée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- Message WM_CAP_FILE_ALLOCATE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464734"
---
# <a name="wm_cap_file_allocate-message"></a><span data-ttu-id="18ee9-105">\_Message d' \_ allocation du fichier WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="18ee9-105">WM\_CAP\_FILE\_ALLOCATE message</span></span>

<span data-ttu-id="18ee9-106">Le **message \_ WM \_ Cap \_ allocate** crée (Préalloue) un fichier de capture d’une taille spécifiée.</span><span class="sxs-lookup"><span data-stu-id="18ee9-106">The **WM\_CAP\_FILE\_ALLOCATE** message creates (preallocates) a capture file of a specified size.</span></span> <span data-ttu-id="18ee9-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .</span><span class="sxs-lookup"><span data-stu-id="18ee9-107">You can send this message explicitly or by using the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro.</span></span>


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a><span data-ttu-id="18ee9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18ee9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ee9-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize nul*</span><span class="sxs-lookup"><span data-stu-id="18ee9-109"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*</span></span>
</dt> <dd>

<span data-ttu-id="18ee9-110">Taille, en octets, pour créer le fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="18ee9-110">Size, in bytes, to create the capture file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ee9-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="18ee9-111">Return Value</span></span>

<span data-ttu-id="18ee9-112">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="18ee9-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="18ee9-113">Si une erreur se produit et qu’une fonction de rappel d’erreur est définie à l’aide du message d' [**\_ erreur WM Cap \_ Set \_ callback \_**](wm-cap-set-callback-error.md) , la fonction de rappel d’erreur est appelée.</span><span class="sxs-lookup"><span data-stu-id="18ee9-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ee9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="18ee9-114">Remarks</span></span>

<span data-ttu-id="18ee9-115">Vous pouvez améliorer considérablement les performances de capture de streaming en préallouant un fichier de capture suffisamment grand pour stocker un clip vidéo entier et en défragmentant le fichier de capture avant de capturer le clip.</span><span class="sxs-lookup"><span data-stu-id="18ee9-115">You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ee9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18ee9-116">Requirements</span></span>



| <span data-ttu-id="18ee9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18ee9-117">Requirement</span></span> | <span data-ttu-id="18ee9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="18ee9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="18ee9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ee9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18ee9-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18ee9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="18ee9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ee9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18ee9-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18ee9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="18ee9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="18ee9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ee9-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ee9-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ee9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18ee9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ee9-126">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="18ee9-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="18ee9-127">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="18ee9-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





