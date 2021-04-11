---
title: Message ICM_DRAW_BEGIN (VFW. h)
description: Le \_ message ICM Draw \_ Begin notifie un pilote de rendu pour préparer le dessin de données.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- Message ICM_DRAW_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942631"
---
# <a name="icm_draw_begin-message"></a><span data-ttu-id="ef696-104">Message de début du \_ dessin ICM \_</span><span class="sxs-lookup"><span data-stu-id="ef696-104">ICM\_DRAW\_BEGIN message</span></span>

<span data-ttu-id="ef696-105">Le message **ICM \_ Draw \_ Begin** notifie un pilote de rendu pour préparer le dessin de données.</span><span class="sxs-lookup"><span data-stu-id="ef696-105">The **ICM\_DRAW\_BEGIN** message notifies a rendering driver to prepare to draw data.</span></span>


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="ef696-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef696-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef696-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span><span class="sxs-lookup"><span data-stu-id="ef696-107"><span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*</span></span>
</dt> <dd>

<span data-ttu-id="ef696-108">Pointeur vers une structure [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) contenant le format d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ef696-108">Pointer to an [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="ef696-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef696-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ef696-110">Taille, en octets, de **ICDRAWBEGIN**.</span><span class="sxs-lookup"><span data-stu-id="ef696-110">Size, in bytes, of **ICDRAWBEGIN**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef696-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef696-111">Return Value</span></span>

<span data-ttu-id="ef696-112">Retourne ICERR \_ OK si le pilote prend en charge le dessin des données à l’écran de la manière spécifiée et le format, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ef696-112">Returns ICERR\_OK if the driver supports drawing the data to the screen in the specified manner and format, or an error code otherwise.</span></span> <span data-ttu-id="ef696-113">Les valeurs d’erreur possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef696-113">Possible error values include the following.</span></span>



| <span data-ttu-id="ef696-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef696-114">Value</span></span>               | <span data-ttu-id="ef696-115">Signification</span><span class="sxs-lookup"><span data-stu-id="ef696-115">Meaning</span></span>                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ef696-116">ICERR \_ BADFORMAT</span><span class="sxs-lookup"><span data-stu-id="ef696-116">ICERR\_BADFORMAT</span></span>    | <span data-ttu-id="ef696-117">Le format d’entrée ou de sortie n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ef696-117">Input or output format is not supported.</span></span>                                      |
| <span data-ttu-id="ef696-118">ICERR \_ NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ef696-118">ICERR\_NOTSUPPORTED</span></span> | <span data-ttu-id="ef696-119">Le pilote ne dessine pas directement sur l’écran ou ne prend pas en charge ce message.</span><span class="sxs-lookup"><span data-stu-id="ef696-119">Driver does not draw directly to the screen or does not support this message.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ef696-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ef696-120">Remarks</span></span>

<span data-ttu-id="ef696-121">Si vous souhaitez que le pilote décompresse les données dans une mémoire tampon, envoyez le message de début de la [**\_ \_ décompression ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="ef696-121">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="ef696-122">Les messages de [**\_ \_ fin**](icm-draw-end.md) de dessin **ICM \_ \_** et ICM ne sont pas imbriqués.</span><span class="sxs-lookup"><span data-stu-id="ef696-122">The **ICM\_DRAW\_BEGIN** and [**ICM\_DRAW\_END**](icm-draw-end.md) messages do not nest.</span></span> <span data-ttu-id="ef696-123">Si votre pilote reçoit **le \_ dessin \_ ICM, commencez** la décompression avec **les nouveaux paramètres \_ \_** pour arrêter la décompression.</span><span class="sxs-lookup"><span data-stu-id="ef696-123">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef696-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef696-124">Requirements</span></span>



| <span data-ttu-id="ef696-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef696-125">Requirement</span></span> | <span data-ttu-id="ef696-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef696-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef696-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef696-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef696-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef696-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ef696-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef696-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef696-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef696-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef696-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef696-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef696-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef696-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef696-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef696-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef696-134">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ef696-134">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ef696-135">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="ef696-135">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





