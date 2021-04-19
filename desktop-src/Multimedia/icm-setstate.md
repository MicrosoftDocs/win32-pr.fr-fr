---
title: Message ICM_SETSTATE (VFW. h)
description: Le \_ message d’ICM SETSTATE indique à un pilote de compression vidéo de définir l’état du compresseur. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- Message ICM_SETSTATE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509953"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="b1bdf-105">Message de la CCI \_ SETSTATE</span><span class="sxs-lookup"><span data-stu-id="b1bdf-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="b1bdf-106">Le message d' **ICM \_ SETSTATE** indique à un pilote de compression vidéo de définir l’état du compresseur.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="b1bdf-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="b1bdf-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="b1bdf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1bdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1bdf-109"><span id="pv"></span><span id="PV"></span>*va*</span><span class="sxs-lookup"><span data-stu-id="b1bdf-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="b1bdf-110">Pointeur vers un bloc de mémoire contenant les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="b1bdf-111">Vous pouvez spécifier la **valeur null** pour ce paramètre pour réinitialiser le compresseur à son état par défaut.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="b1bdf-112"><span id="cb"></span><span id="CB"></span>*libéré*</span><span class="sxs-lookup"><span data-stu-id="b1bdf-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="b1bdf-113">Taille, en octets, du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1bdf-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b1bdf-114">Return Value</span></span>

<span data-ttu-id="b1bdf-115">Retourne le nombre d’octets utilisés par le compresseur en cas de réussite ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1bdf-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b1bdf-116">Remarks</span></span>

<span data-ttu-id="b1bdf-117">Les informations utilisées par ce message sont privées et spécifiques à un compresseur donné.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="b1bdf-118">Les applications clientes doivent utiliser ce message uniquement pour restaurer les informations précédemment obtenues avec le message [**\_ GETSTATE ICM**](icm-getstate.md) et doivent utiliser le message de [**\_ configuration ICM**](icm-configure.md) pour ajuster la configuration d’un pilote de compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="b1bdf-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1bdf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1bdf-119">Requirements</span></span>



| <span data-ttu-id="b1bdf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1bdf-120">Requirement</span></span> | <span data-ttu-id="b1bdf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1bdf-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b1bdf-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1bdf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1bdf-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1bdf-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b1bdf-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1bdf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1bdf-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1bdf-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b1bdf-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1bdf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1bdf-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1bdf-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1bdf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1bdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1bdf-129">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="b1bdf-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b1bdf-130">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="b1bdf-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





