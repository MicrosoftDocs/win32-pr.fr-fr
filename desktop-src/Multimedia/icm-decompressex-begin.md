---
title: Message ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: Le \_ message DECOMPRESSEX de \_ début ICM indique à un pilote de compression vidéo de préparer la décompression des données.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- Message ICM_DECOMPRESSEX_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742956"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="ce8ae-104">Message de début de \_ DECOMPRESSEX ICM \_</span><span class="sxs-lookup"><span data-stu-id="ce8ae-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="ce8ae-105">Le **message \_ DECOMPRESSEX de \_ début ICM** indique à un pilote de compression vidéo de préparer la décompression des données.</span><span class="sxs-lookup"><span data-stu-id="ce8ae-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="ce8ae-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce8ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce8ae-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="ce8ae-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="ce8ae-108">Pointeur vers une structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenant les formats d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="ce8ae-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="ce8ae-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce8ae-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ce8ae-110">Taille, en octets, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="ce8ae-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce8ae-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce8ae-111">Return Value</span></span>

<span data-ttu-id="ce8ae-112">Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ce8ae-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce8ae-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ce8ae-113">Remarks</span></span>

<span data-ttu-id="ce8ae-114">Lorsque le pilote reçoit ce message, il doit allouer des tampons et effectuer des opérations qui prennent du temps pour pouvoir traiter efficacement les messages [**\_ DECOMPRESSEX ICM**](icm-decompressex.md) .</span><span class="sxs-lookup"><span data-stu-id="ce8ae-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="ce8ae-115">Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message d’accueil de [**\_ \_ dessin ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="ce8ae-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="ce8ae-116">Les messages End **\_ DECOMPRESSEX \_ Begin** et [**ICM \_ DECOMPRESSEX \_ end**](icm-decompressex-end.md) ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="ce8ae-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="ce8ae-117">Si votre pilote reçoit **des \_ DECOMPRESSEX \_ ICM** avant que la décompression ne soit arrêtée avec l' **\_ \_ extrémité DECOMPRESSEX ICM**, il doit redémarrer la décompression avec les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="ce8ae-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce8ae-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce8ae-118">Requirements</span></span>



| <span data-ttu-id="ce8ae-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce8ae-119">Requirement</span></span> | <span data-ttu-id="ce8ae-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce8ae-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ce8ae-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce8ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce8ae-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce8ae-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ce8ae-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce8ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce8ae-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce8ae-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce8ae-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce8ae-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce8ae-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce8ae-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce8ae-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce8ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce8ae-128">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ce8ae-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ce8ae-129">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ce8ae-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





