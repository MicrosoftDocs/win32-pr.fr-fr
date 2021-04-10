---
title: Message DRV_QUERYCONFIGURE (mmsystem. h)
description: Indique au pilote de spécifier s’il prend en charge la configuration personnalisée.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- Message DRV_QUERYCONFIGURE Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200576"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="9a1c0-104">\_Message QUERYCONFIGURE</span><span class="sxs-lookup"><span data-stu-id="9a1c0-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="9a1c0-105">Indique au pilote de spécifier s’il prend en charge la configuration personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9a1c0-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a1c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a1c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a1c0-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="9a1c0-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="9a1c0-108">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="9a1c0-108">Identifier of the installable driver.</span></span> <span data-ttu-id="9a1c0-109">Il s’agit de la même valeur que celle précédemment retournée par le pilote à partir du message de l' [**\_ ouverture du DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="9a1c0-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="9a1c0-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="9a1c0-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="9a1c0-111">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="9a1c0-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a1c0-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a1c0-112">Return Value</span></span>

<span data-ttu-id="9a1c0-113">Retourne une valeur différente de zéro si le pilote peut afficher une boîte de dialogue de configuration ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9a1c0-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a1c0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9a1c0-114">Remarks</span></span>

<span data-ttu-id="9a1c0-115">Les paramètres *lParam1* et *lParam2* ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="9a1c0-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a1c0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a1c0-116">Requirements</span></span>



| <span data-ttu-id="9a1c0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a1c0-117">Requirement</span></span> | <span data-ttu-id="9a1c0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a1c0-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a1c0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a1c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9a1c0-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a1c0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a1c0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a1c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9a1c0-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a1c0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a1c0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a1c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a1c0-124"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a1c0-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a1c0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a1c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1c0-126">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="9a1c0-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="9a1c0-127">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="9a1c0-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





