---
title: Message DRV_OPEN (mmsystem. h)
description: Indique au pilote d’ouvrir une nouvelle instance.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- Message DRV_OPEN Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106222"
---
# <a name="drv_open-message"></a><span data-ttu-id="a1913-104">DRV \_ message ouvert</span><span class="sxs-lookup"><span data-stu-id="a1913-104">DRV\_OPEN message</span></span>

<span data-ttu-id="a1913-105">Indique au pilote d’ouvrir une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="a1913-105">Directs the driver to open an new instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1913-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1913-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1913-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="a1913-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="a1913-108">Identificateur du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="a1913-108">Identifier of the installable driver.</span></span>

</dd> <dt>

<span data-ttu-id="a1913-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="a1913-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="a1913-110">Handle de l’instance du pilote installable.</span><span class="sxs-lookup"><span data-stu-id="a1913-110">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="a1913-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a1913-111"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a1913-112">Adresse d’une chaîne de caractères larges se terminant par un caractère null qui spécifie les informations de configuration utilisées pour ouvrir l’instance.</span><span class="sxs-lookup"><span data-stu-id="a1913-112">Address of a null-terminated, wide-character string that specifies configuration information used to open the instance.</span></span> <span data-ttu-id="a1913-113">Si aucune information de configuration n’est disponible, soit cette chaîne est vide, soit le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a1913-113">If no configuration information is available, either this string is empty or the parameter is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a1913-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a1913-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a1913-115">données spécifiques au pilote 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a1913-115">32-bit driver-specific data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1913-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a1913-116">Return Value</span></span>

<span data-ttu-id="a1913-117">Retourne une valeur différente de zéro en cas de réussite ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1913-117">Returns a nonzero value if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1913-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a1913-118">Remarks</span></span>

<span data-ttu-id="a1913-119">Si le pilote retourne une valeur différente de zéro, le système utilise cette valeur comme identificateur de pilote (le paramètre *dwDriverId* ) dans les messages qu’il envoie par la suite à l’instance du pilote.</span><span class="sxs-lookup"><span data-stu-id="a1913-119">If the driver returns a nonzero value, the system uses that value as the driver identifier (the *dwDriverId* parameter) in messages it subsequently sends to the driver instance.</span></span> <span data-ttu-id="a1913-120">Le pilote peut retourner n’importe quel type de valeur comme identificateur.</span><span class="sxs-lookup"><span data-stu-id="a1913-120">The driver can return any type of value as the identifier.</span></span> <span data-ttu-id="a1913-121">Par exemple, certains pilotes retournent des adresses mémoire qui pointent vers des informations spécifiques à l’instance.</span><span class="sxs-lookup"><span data-stu-id="a1913-121">For example, some drivers return memory addresses that point to instance-specific information.</span></span> <span data-ttu-id="a1913-122">L’utilisation de cette méthode de spécification des identificateurs pour une instance de pilote permet aux pilotes d’accéder aux informations pendant qu’ils traitent des messages.</span><span class="sxs-lookup"><span data-stu-id="a1913-122">Using this method of specifying identifiers for a driver instance gives the drivers ready access to the information while they are processing messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1913-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1913-123">Requirements</span></span>



| <span data-ttu-id="a1913-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1913-124">Requirement</span></span> | <span data-ttu-id="a1913-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1913-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1913-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1913-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1913-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1913-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a1913-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1913-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1913-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1913-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a1913-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1913-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1913-131"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1913-131"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1913-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1913-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1913-133">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="a1913-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="a1913-134">Messages de pilote installables</span><span class="sxs-lookup"><span data-stu-id="a1913-134">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





