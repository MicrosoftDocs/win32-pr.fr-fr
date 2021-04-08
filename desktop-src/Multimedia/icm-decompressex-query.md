---
title: Message ICM_DECOMPRESSEX_QUERY (VFW. h)
description: Le \_ message de \_ requête DECOMPRESSEX ICM interroge un pilote de compression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- Message ICM_DECOMPRESSEX_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844069"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="eddfe-104">\_Message de \_ requête DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="eddfe-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="eddfe-105">Le message de **\_ \_ requête DECOMPRESSEX ICM** interroge un pilote de compression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.</span><span class="sxs-lookup"><span data-stu-id="eddfe-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="eddfe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eddfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eddfe-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="eddfe-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="eddfe-108">Pointeur vers une structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="eddfe-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="eddfe-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="eddfe-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="eddfe-110">Taille, en octets, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="eddfe-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eddfe-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eddfe-111">Return Value</span></span>

<span data-ttu-id="eddfe-112">Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="eddfe-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="eddfe-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eddfe-113">Requirements</span></span>



| <span data-ttu-id="eddfe-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eddfe-114">Requirement</span></span> | <span data-ttu-id="eddfe-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="eddfe-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="eddfe-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddfe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eddfe-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eddfe-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eddfe-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eddfe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eddfe-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eddfe-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eddfe-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="eddfe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eddfe-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="eddfe-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eddfe-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eddfe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eddfe-123">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="eddfe-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="eddfe-124">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="eddfe-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





