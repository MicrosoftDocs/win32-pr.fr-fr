---
title: Message ICM_DECOMPRESS_QUERY (VFW. h)
description: Le message de requête de décompression ICM \_ \_ interroge un pilote de décompression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- Message ICM_DECOMPRESS_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511585"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="6e900-104">\_Message de requête de décompression ICM \_</span><span class="sxs-lookup"><span data-stu-id="6e900-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="6e900-105">Le message de **\_ \_ requête** de décompression ICM interroge un pilote de décompression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.</span><span class="sxs-lookup"><span data-stu-id="6e900-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="6e900-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .</span><span class="sxs-lookup"><span data-stu-id="6e900-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="6e900-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e900-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e900-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="6e900-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="6e900-109">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6e900-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="6e900-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="6e900-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="6e900-111">Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format de sortie.</span><span class="sxs-lookup"><span data-stu-id="6e900-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="6e900-112">Vous pouvez spécifier zéro pour ce paramètre pour indiquer qu’un format de sortie est acceptable.</span><span class="sxs-lookup"><span data-stu-id="6e900-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e900-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e900-113">Return Value</span></span>

<span data-ttu-id="6e900-114">Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6e900-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e900-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e900-115">Requirements</span></span>



| <span data-ttu-id="6e900-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6e900-116">Requirement</span></span> | <span data-ttu-id="6e900-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6e900-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6e900-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e900-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6e900-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e900-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6e900-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6e900-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6e900-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6e900-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6e900-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6e900-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e900-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e900-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e900-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e900-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e900-125">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="6e900-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6e900-126">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="6e900-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

