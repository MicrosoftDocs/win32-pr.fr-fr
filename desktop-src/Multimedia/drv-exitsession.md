---
title: Message DRV_EXITSESSION (mmsystem. h)
description: Avertit le pilote que Windows se prépare à quitter. Le pilote doit se préparer à l’arrêt.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- Message DRV_EXITSESSION Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466930"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="ae462-105">\_Message EXITSESSION</span><span class="sxs-lookup"><span data-stu-id="ae462-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="ae462-106">Avertit le pilote que Windows se prépare à quitter.</span><span class="sxs-lookup"><span data-stu-id="ae462-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="ae462-107">Le pilote doit se préparer à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ae462-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae462-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae462-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae462-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="ae462-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="ae462-110">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="ae462-110">Identifier of the installable driver.</span></span> <span data-ttu-id="ae462-111">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="ae462-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="ae462-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="ae462-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="ae462-113">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="ae462-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae462-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae462-114">Return Value</span></span>

<span data-ttu-id="ae462-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ae462-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae462-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ae462-116">Remarks</span></span>

<span data-ttu-id="ae462-117">Les paramètres *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="ae462-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae462-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae462-118">Requirements</span></span>



| <span data-ttu-id="ae462-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae462-119">Requirement</span></span> | <span data-ttu-id="ae462-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae462-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae462-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae462-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ae462-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae462-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ae462-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae462-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ae462-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae462-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ae462-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae462-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae462-126"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae462-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae462-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae462-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae462-128">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="ae462-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="ae462-129">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="ae462-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





