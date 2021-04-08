---
title: Message ICM_GET (VFW. h)
description: Le \_ message d’extraction ICM récupère une valeur DWORD définie par l’application à partir d’un pilote de compression vidéo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- Message ICM_GET Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740493"
---
# <a name="icm_get-message"></a><span data-ttu-id="431e1-104">\_Message d’extraction ICM</span><span class="sxs-lookup"><span data-stu-id="431e1-104">ICM\_GET message</span></span>

<span data-ttu-id="431e1-105">Le message d' **\_ extraction ICM** récupère une valeur **DWORD** définie par l’application à partir d’un pilote de compression vidéo.</span><span class="sxs-lookup"><span data-stu-id="431e1-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="431e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="431e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431e1-107"><span id="pv"></span><span id="PV"></span>*va*</span><span class="sxs-lookup"><span data-stu-id="431e1-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="431e1-108">Pointeur vers un bloc de mémoire à remplir avec l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="431e1-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="431e1-109">Vous pouvez également spécifier la **valeur null** pour déterminer la quantité de mémoire requise par les informations d’État.</span><span class="sxs-lookup"><span data-stu-id="431e1-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="431e1-110"><span id="cb"></span><span id="CB"></span>*libéré*</span><span class="sxs-lookup"><span data-stu-id="431e1-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="431e1-111">Taille, en octets, du bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="431e1-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431e1-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="431e1-112">Return Value</span></span>

<span data-ttu-id="431e1-113">Retourne la quantité de mémoire, en octets, requise pour stocker les informations d’État.</span><span class="sxs-lookup"><span data-stu-id="431e1-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="431e1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="431e1-114">Remarks</span></span>

<span data-ttu-id="431e1-115">La structure utilisée pour représenter les informations d’État est spécifique au pilote et est définie par le pilote.</span><span class="sxs-lookup"><span data-stu-id="431e1-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="431e1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="431e1-116">Requirements</span></span>



| <span data-ttu-id="431e1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="431e1-117">Requirement</span></span> | <span data-ttu-id="431e1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="431e1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="431e1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="431e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="431e1-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="431e1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="431e1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="431e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="431e1-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="431e1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="431e1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="431e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="431e1-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="431e1-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431e1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="431e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431e1-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="431e1-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="431e1-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="431e1-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





