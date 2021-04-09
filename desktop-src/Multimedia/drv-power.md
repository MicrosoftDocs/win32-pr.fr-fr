---
title: Message DRV_POWER (mmsystem. h)
description: Informe le pilote que l’alimentation de l’appareil est activée ou désactivée.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- Message DRV_POWER Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942823"
---
# <a name="drv_power-message"></a><span data-ttu-id="01c6e-104">\_Message d’alimentation du DRV</span><span class="sxs-lookup"><span data-stu-id="01c6e-104">DRV\_POWER message</span></span>

<span data-ttu-id="01c6e-105">Informe le pilote que l’alimentation de l’appareil est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="01c6e-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="01c6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01c6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c6e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="01c6e-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="01c6e-108">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="01c6e-108">Identifier of the installable driver.</span></span> <span data-ttu-id="01c6e-109">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="01c6e-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="01c6e-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="01c6e-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="01c6e-111">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="01c6e-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c6e-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="01c6e-112">Return Value</span></span>

<span data-ttu-id="01c6e-113">Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="01c6e-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c6e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="01c6e-114">Remarks</span></span>

<span data-ttu-id="01c6e-115">Les paramètres *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="01c6e-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c6e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01c6e-116">Requirements</span></span>



| <span data-ttu-id="01c6e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01c6e-117">Requirement</span></span> | <span data-ttu-id="01c6e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="01c6e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c6e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01c6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="01c6e-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01c6e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="01c6e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01c6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="01c6e-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01c6e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="01c6e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="01c6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c6e-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01c6e-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c6e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01c6e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c6e-126">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="01c6e-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="01c6e-127">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="01c6e-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





