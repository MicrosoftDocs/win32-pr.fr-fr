---
title: Message DRV_REMOVE (mmsystem. h)
description: Indique au pilote qu’il va être supprimé du système. Lorsqu’un pilote reçoit ce message, il doit supprimer toutes les sections qu’il a créées dans le registre.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- Message DRV_REMOVE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033241"
---
# <a name="drv_remove-message"></a><span data-ttu-id="5bbef-105">DRV \_ supprimer le message</span><span class="sxs-lookup"><span data-stu-id="5bbef-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="5bbef-106">Indique au pilote qu’il va être supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="5bbef-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="5bbef-107">Lorsqu’un pilote reçoit ce message, il doit supprimer toutes les sections qu’il a créées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5bbef-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bbef-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bbef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbef-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="5bbef-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="5bbef-110">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="5bbef-110">Identifier of the installable driver.</span></span> <span data-ttu-id="5bbef-111">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="5bbef-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="5bbef-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="5bbef-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="5bbef-113">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="5bbef-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bbef-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5bbef-114">Return Value</span></span>

<span data-ttu-id="5bbef-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5bbef-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bbef-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5bbef-116">Remarks</span></span>

<span data-ttu-id="5bbef-117">Les paramètres *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="5bbef-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbef-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bbef-118">Requirements</span></span>



| <span data-ttu-id="5bbef-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bbef-119">Requirement</span></span> | <span data-ttu-id="5bbef-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bbef-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbef-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bbef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbef-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bbef-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5bbef-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bbef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbef-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bbef-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5bbef-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bbef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bbef-126"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bbef-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbef-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bbef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bbef-128">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="5bbef-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="5bbef-129">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="5bbef-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





