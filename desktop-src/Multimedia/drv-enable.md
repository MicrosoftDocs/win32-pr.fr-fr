---
title: Message DRV_ENABLE (mmsystem. h)
description: Active le pilote. Le pilote doit initialiser toutes les variables et localiser les appareils avec l’interface d’entrée et de sortie (e/s).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- Message DRV_ENABLE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942830"
---
# <a name="drv_enable-message"></a><span data-ttu-id="8ae6d-105">DRV- \_ activer le message</span><span class="sxs-lookup"><span data-stu-id="8ae6d-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="8ae6d-106">Active le pilote.</span><span class="sxs-lookup"><span data-stu-id="8ae6d-106">Enables the driver.</span></span> <span data-ttu-id="8ae6d-107">Le pilote doit initialiser toutes les variables et localiser les appareils avec l’interface d’entrée et de sortie (e/s).</span><span class="sxs-lookup"><span data-stu-id="8ae6d-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ae6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ae6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae6d-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="8ae6d-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="8ae6d-110">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="8ae6d-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae6d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8ae6d-111">Return Value</span></span>

<span data-ttu-id="8ae6d-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8ae6d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae6d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="8ae6d-113">Remarks</span></span>

<span data-ttu-id="8ae6d-114">Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="8ae6d-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="8ae6d-115">Les pilotes sont considérés comme activés à partir du moment où ils reçoivent ce message jusqu’à ce qu’ils soient désactivés à l’aide du message de [**\_ désactivation DRV**](drv-disable.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae6d-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae6d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ae6d-116">Requirements</span></span>



| <span data-ttu-id="8ae6d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ae6d-117">Requirement</span></span> | <span data-ttu-id="8ae6d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ae6d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae6d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae6d-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ae6d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ae6d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ae6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae6d-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ae6d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ae6d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ae6d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ae6d-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae6d-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae6d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ae6d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae6d-126">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="8ae6d-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="8ae6d-127">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="8ae6d-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





