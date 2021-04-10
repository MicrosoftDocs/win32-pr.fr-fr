---
title: Message DRV_FREE (mmsystem. h)
description: Avertit le pilote qu’il est en cours de suppression de la mémoire. Le pilote doit libérer la mémoire et les autres ressources système qu’il a allouées.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- Message DRV_FREE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942827"
---
# <a name="drv_free-message"></a><span data-ttu-id="603ee-105">\_Message Free DRV</span><span class="sxs-lookup"><span data-stu-id="603ee-105">DRV\_FREE message</span></span>

<span data-ttu-id="603ee-106">Avertit le pilote qu’il est en cours de suppression de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="603ee-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="603ee-107">Le pilote doit libérer la mémoire et les autres ressources système qu’il a allouées.</span><span class="sxs-lookup"><span data-stu-id="603ee-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="603ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="603ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603ee-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="603ee-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="603ee-110">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="603ee-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603ee-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="603ee-111">Return Value</span></span>

<span data-ttu-id="603ee-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="603ee-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="603ee-113">Notes</span><span class="sxs-lookup"><span data-stu-id="603ee-113">Remarks</span></span>

<span data-ttu-id="603ee-114">Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="603ee-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="603ee-115">Le **message \_ Free DRV** est toujours le dernier message reçu par un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="603ee-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="603ee-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="603ee-116">Requirements</span></span>



| <span data-ttu-id="603ee-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="603ee-117">Requirement</span></span> | <span data-ttu-id="603ee-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="603ee-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="603ee-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="603ee-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603ee-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="603ee-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="603ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="603ee-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="603ee-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="603ee-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="603ee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="603ee-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="603ee-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603ee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603ee-126">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="603ee-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="603ee-127">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="603ee-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





