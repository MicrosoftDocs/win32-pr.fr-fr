---
title: Message DRV_CLOSE (mmsystem. h)
description: Indique au pilote de fermer l’instance donnée. Si aucune autre instance n’est ouverte, le pilote doit préparer la mise en version suivante à partir de la mémoire.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- Message DRV_CLOSE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509947"
---
# <a name="drv_close-message"></a><span data-ttu-id="516e3-105">Message de fermeture du DRV \_</span><span class="sxs-lookup"><span data-stu-id="516e3-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="516e3-106">Indique au pilote de fermer l’instance donnée.</span><span class="sxs-lookup"><span data-stu-id="516e3-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="516e3-107">Si aucune autre instance n’est ouverte, le pilote doit préparer la mise en version suivante à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="516e3-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="516e3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="516e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516e3-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="516e3-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="516e3-110">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="516e3-110">Identifier of the installable driver.</span></span> <span data-ttu-id="516e3-111">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="516e3-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="516e3-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="516e3-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="516e3-113">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="516e3-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="516e3-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="516e3-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="516e3-115">valeur 32 bits spécifiée comme paramètre *lParam1* dans un appel à la fonction **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="516e3-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="516e3-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="516e3-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="516e3-117">valeur 32 bits spécifiée comme paramètre *lParam2* dans un appel à la fonction **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="516e3-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516e3-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="516e3-118">Return Value</span></span>

<span data-ttu-id="516e3-119">Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="516e3-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="516e3-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="516e3-120">Requirements</span></span>



| <span data-ttu-id="516e3-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="516e3-121">Requirement</span></span> | <span data-ttu-id="516e3-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="516e3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="516e3-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="516e3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="516e3-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="516e3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="516e3-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="516e3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="516e3-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="516e3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="516e3-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="516e3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="516e3-128"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="516e3-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516e3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="516e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516e3-130">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="516e3-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="516e3-131">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="516e3-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





