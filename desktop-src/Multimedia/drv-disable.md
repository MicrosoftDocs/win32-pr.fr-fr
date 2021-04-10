---
title: Message DRV_DISABLE (mmsystem. h)
description: Désactive le pilote. Le pilote doit placer l’appareil correspondant, le cas échéant, dans un état inactif et terminer les fonctions de rappel ou les threads.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- Message DRV_DISABLE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942828"
---
# <a name="drv_disable-message"></a><span data-ttu-id="48765-105">DRV- \_ message de désactivation</span><span class="sxs-lookup"><span data-stu-id="48765-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="48765-106">Désactive le pilote.</span><span class="sxs-lookup"><span data-stu-id="48765-106">Disables the driver.</span></span> <span data-ttu-id="48765-107">Le pilote doit placer l’appareil correspondant, le cas échéant, dans un état inactif et terminer les fonctions de rappel ou les threads.</span><span class="sxs-lookup"><span data-stu-id="48765-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="48765-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48765-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48765-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="48765-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="48765-110">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="48765-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48765-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="48765-111">Return Value</span></span>

<span data-ttu-id="48765-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="48765-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48765-113">Notes</span><span class="sxs-lookup"><span data-stu-id="48765-113">Remarks</span></span>

<span data-ttu-id="48765-114">Les paramètres *dwDriverId*, *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="48765-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="48765-115">Après la désactivation du pilote, le système envoie généralement au pilote un message de fin de la commande [**DRV \_**](drv-free.md) avant de supprimer le pilote de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="48765-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="48765-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48765-116">Requirements</span></span>



| <span data-ttu-id="48765-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48765-117">Requirement</span></span> | <span data-ttu-id="48765-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="48765-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48765-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48765-119">Minimum supported client</span></span><br/> | <span data-ttu-id="48765-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48765-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="48765-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48765-121">Minimum supported server</span></span><br/> | <span data-ttu-id="48765-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="48765-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="48765-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="48765-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="48765-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48765-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48765-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48765-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48765-126">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="48765-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="48765-127">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="48765-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





