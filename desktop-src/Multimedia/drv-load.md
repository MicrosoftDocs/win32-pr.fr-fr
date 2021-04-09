---
title: Message DRV_LOAD (mmsystem. h)
description: Notifie le pilote qu’il a été chargé. Le pilote doit s’assurer que tout le matériel et les pilotes de prise en charge dont il a besoin pour fonctionner correctement sont présents.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- Message DRV_LOAD Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942825"
---
# <a name="drv_load-message"></a><span data-ttu-id="80498-105">Le \_ message de chargement du DRV</span><span class="sxs-lookup"><span data-stu-id="80498-105">DRV\_LOAD message</span></span>

<span data-ttu-id="80498-106">Notifie le pilote qu’il a été chargé.</span><span class="sxs-lookup"><span data-stu-id="80498-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="80498-107">Le pilote doit s’assurer que tout le matériel et les pilotes de prise en charge dont il a besoin pour fonctionner correctement sont présents.</span><span class="sxs-lookup"><span data-stu-id="80498-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="80498-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80498-108">Parameters</span></span>

<span data-ttu-id="80498-109">Le paramètre *hdrvr* est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="80498-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="80498-110">Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="80498-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="80498-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="80498-111">Return Value</span></span>

<span data-ttu-id="80498-112">Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="80498-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="80498-113">Notes</span><span class="sxs-lookup"><span data-stu-id="80498-113">Remarks</span></span>

<span data-ttu-id="80498-114">Le message de **\_ chargement du DRV** est toujours le premier message reçu par un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="80498-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="80498-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80498-115">Requirements</span></span>



| <span data-ttu-id="80498-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80498-116">Requirement</span></span> | <span data-ttu-id="80498-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="80498-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80498-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80498-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80498-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80498-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80498-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80498-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80498-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80498-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80498-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="80498-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80498-123"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80498-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80498-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80498-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80498-125">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="80498-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="80498-126">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="80498-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





