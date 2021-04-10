---
title: Message ICM_GETSTATE (VFW. h)
description: Le \_ message GETSTATE ICM interroge un pilote de compression vidéo pour retourner sa configuration actuelle dans un bloc de mémoire ou pour déterminer la quantité de mémoire nécessaire pour récupérer les informations de configuration.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- Message ICM_GETSTATE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106549"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="0f5e2-104">\_Message GETSTATE ICM</span><span class="sxs-lookup"><span data-stu-id="0f5e2-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="0f5e2-105">Le **message \_ GETSTATE ICM** interroge un pilote de compression vidéo pour retourner sa configuration actuelle dans un bloc de mémoire ou pour déterminer la quantité de mémoire nécessaire pour récupérer les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="0f5e2-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="0f5e2-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="0f5e2-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="0f5e2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f5e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5e2-108"><span id="pv"></span><span id="PV"></span>*va*</span><span class="sxs-lookup"><span data-stu-id="0f5e2-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="0f5e2-109">Pointeur vers un bloc de mémoire destiné à contenir les informations de configuration actuelles.</span><span class="sxs-lookup"><span data-stu-id="0f5e2-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="0f5e2-110">Vous pouvez spécifier la **valeur null** pour ce paramètre afin de déterminer la quantité de mémoire requise pour les informations de configuration, comme dans [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span><span class="sxs-lookup"><span data-stu-id="0f5e2-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="0f5e2-111"><span id="cb"></span><span id="CB"></span>*libéré*</span><span class="sxs-lookup"><span data-stu-id="0f5e2-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="0f5e2-112">Taille, en octets, du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0f5e2-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5e2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f5e2-113">Return Value</span></span>

<span data-ttu-id="0f5e2-114">Si *PV* est **null**, retourne la quantité de mémoire, en octets, requise pour les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="0f5e2-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="0f5e2-115">Si *PV* n’est pas **null**, retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0f5e2-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f5e2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0f5e2-116">Remarks</span></span>

<span data-ttu-id="0f5e2-117">La structure utilisée pour représenter les informations de configuration est spécifique au pilote et est définie par le pilote.</span><span class="sxs-lookup"><span data-stu-id="0f5e2-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5e2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f5e2-118">Requirements</span></span>



| <span data-ttu-id="0f5e2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f5e2-119">Requirement</span></span> | <span data-ttu-id="0f5e2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f5e2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0f5e2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f5e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5e2-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f5e2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0f5e2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f5e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5e2-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f5e2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f5e2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f5e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f5e2-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5e2-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f5e2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f5e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5e2-128">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="0f5e2-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0f5e2-129">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="0f5e2-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





