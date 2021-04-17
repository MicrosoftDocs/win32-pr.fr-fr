---
title: Message ICM_DECOMPRESSEX_END (VFW. h)
description: Le \_ message de \_ fin DECOMPRESSEX ICM indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- Message ICM_DECOMPRESSEX_END Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509150"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="bd49c-105">\_Message de \_ fin DECOMPRESSEX ICM</span><span class="sxs-lookup"><span data-stu-id="bd49c-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="bd49c-106">Le message de **\_ \_ fin DECOMPRESSEX ICM** indique à un pilote de décompression vidéo de terminer la décompression et de libérer les ressources allouées pour la décompression.</span><span class="sxs-lookup"><span data-stu-id="bd49c-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="bd49c-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .</span><span class="sxs-lookup"><span data-stu-id="bd49c-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="bd49c-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bd49c-108">Return Value</span></span>

<span data-ttu-id="bd49c-109">Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bd49c-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd49c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bd49c-110">Remarks</span></span>

<span data-ttu-id="bd49c-111">Le pilote libère toutes les ressources allouées pour le message de [**\_ \_ début DECOMPRESSEX ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="bd49c-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="bd49c-112">[**ICM \_ Les \_**](icm-decompressex-begin.md) **\_ \_ terminaisons** DECOMPRESSEX Begin et ICM DECOMPRESSEX ne sont pas imbriquées.</span><span class="sxs-lookup"><span data-stu-id="bd49c-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="bd49c-113">Si votre pilote reçoit **des \_ DECOMPRESSEX \_ ICM** avant que la décompression ne soit arrêtée avec l' **\_ \_ extrémité DECOMPRESSEX ICM**, il doit redémarrer la décompression avec les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="bd49c-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd49c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd49c-114">Requirements</span></span>



| <span data-ttu-id="bd49c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd49c-115">Requirement</span></span> | <span data-ttu-id="bd49c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd49c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bd49c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd49c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd49c-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd49c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bd49c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd49c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd49c-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd49c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bd49c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd49c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd49c-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd49c-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd49c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd49c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd49c-124">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="bd49c-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="bd49c-125">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="bd49c-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





