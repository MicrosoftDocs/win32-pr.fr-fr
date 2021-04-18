---
description: Les \_ constantes LINEFEATURE répertorient les opérations qui peuvent être appelées sur une ligne à l’aide de cette API.
ms.assetid: 77fa313c-e720-4607-b691-51b5be76ceed
title: Constantes LINEFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac930123a10f401a7a79de8ccf6c61452df05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526890"
---
# <a name="linefeature_-constants"></a><span data-ttu-id="ff690-103">\_Constantes LINEFEATURE</span><span class="sxs-lookup"><span data-stu-id="ff690-103">LINEFEATURE\_ Constants</span></span>

<span data-ttu-id="ff690-104">Les **\_ constantes LINEFEATURE** répertorient les opérations qui peuvent être appelées sur une ligne à l’aide de cette API.</span><span class="sxs-lookup"><span data-stu-id="ff690-104">The **LINEFEATURE\_ constants** list the operations that can be invoked on a line using this API.</span></span>

<dl> <dt>

<span data-ttu-id="ff690-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="ff690-105"><span id="LINEFEATURE_DEVSPECIFIC"></span><span id="linefeature_devspecific"></span>**LINEFEATURE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-106">Les opérations spécifiques au périphérique peuvent être utilisées sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-106">Device-specific operations can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE \_ DEVSPECIFICFEAT**</span><span class="sxs-lookup"><span data-stu-id="ff690-107"><span id="LINEFEATURE_DEVSPECIFICFEAT"></span><span id="linefeature_devspecificfeat"></span>**LINEFEATURE\_DEVSPECIFICFEAT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-108">Les fonctionnalités spécifiques au périphérique peuvent être utilisées sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-108">Device-specific features can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE \_ vers l’avant**</span><span class="sxs-lookup"><span data-stu-id="ff690-109"><span id="LINEFEATURE_FORWARD"></span><span id="linefeature_forward"></span>**LINEFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-110">Le transfert de toutes les adresses peut être utilisé sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-110">Forwarding of all addresses can be used on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="ff690-111"><span id="LINEFEATURE_FORWARDDND"></span><span id="linefeature_forwarddnd"></span>**LINEFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-112">La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (avec une adresse de destination vide) peut être utilisée pour activer la fonctionnalité ne pas déranger sur toutes les adresses sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-112">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on all addresses on the line.</span></span> <span data-ttu-id="ff690-113">LINEFEATURE \_ Forward sera également défini.</span><span class="sxs-lookup"><span data-stu-id="ff690-113">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="ff690-114">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="ff690-114">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="ff690-115"><span id="LINEFEATURE_FORWARDFWD"></span><span id="linefeature_forwardfwd"></span>**LINEFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-116">La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) peut être utilisée pour transférer des appels sur toute adresse sur la ligne à d’autres nombres.</span><span class="sxs-lookup"><span data-stu-id="ff690-116">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on all address on the line to other numbers.</span></span> <span data-ttu-id="ff690-117">LINEFEATURE \_ Forward sera également défini.</span><span class="sxs-lookup"><span data-stu-id="ff690-117">LINEFEATURE\_FORWARD will also be set.</span></span> <span data-ttu-id="ff690-118">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="ff690-118">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="ff690-119"><span id="LINEFEATURE_MAKECALL"></span><span id="linefeature_makecall"></span>**LINEFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-120">Un appel sortant peut être placé sur cette ligne à l’aide d’une adresse non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ff690-120">An outgoing call can be placed on this line using an unspecified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE \_ SETDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ff690-121"><span id="LINEFEATURE_SETDEVSTATUS"></span><span id="linefeature_setdevstatus"></span>**LINEFEATURE\_SETDEVSTATUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-122">La fonction [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) peut être appelée sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-122">The [**lineSetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) function can be invoked on the line device.</span></span> <span data-ttu-id="ff690-123">Cet indicateur est exposé uniquement aux applications qui négocient une version TAPI 2,0 ou supérieure.</span><span class="sxs-lookup"><span data-stu-id="ff690-123">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="ff690-124"><span id="LINEFEATURE_SETMEDIACONTROL"></span><span id="linefeature_setmediacontrol"></span>**LINEFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-125">Le contrôle de média peut être défini sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-125">Media control can be set on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ff690-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE \_ SETTERMINAL**</span><span class="sxs-lookup"><span data-stu-id="ff690-126"><span id="LINEFEATURE_SETTERMINAL"></span><span id="linefeature_setterminal"></span>**LINEFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ff690-127">Les modes de terminal pour cette ligne peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="ff690-127">Terminal modes for this line can be set.</span></span>

> [!Note]  
> <span data-ttu-id="ff690-128">Si aucun des nouveaux bits « FORWARD » modifiés n’est défini dans le membre **dwLineFeatures** dans [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) , mais que le \_ bit de transfert LINEFEATURE est défini, l’un des modes Forward peut fonctionner ; le fournisseur de services n’a simplement pas spécifié les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="ff690-128">If neither of the new modified "FORWARD" bits is set in the **dwLineFeatures** member in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) but the LINEFEATURE\_FORWARD bit is set, then any of the forward modes can work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff690-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ff690-129">Remarks</span></span>

<span data-ttu-id="ff690-130">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="ff690-130">No extensibility.</span></span> <span data-ttu-id="ff690-131">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="ff690-131">All 32 bits are reserved.</span></span>

<span data-ttu-id="ff690-132">Les \_ constantes LINEFEATURE sont utilisées dans [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (retourné par [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span><span class="sxs-lookup"><span data-stu-id="ff690-132">The LINEFEATURE\_ constants are used in [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) (returned by [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)).</span></span> <span data-ttu-id="ff690-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) signale, pour une ligne donnée, les fonctionnalités de ligne qui peuvent être appelées alors que la ligne est à l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="ff690-133">[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) reports, for a given line, which line features can actually be invoked while the line is in the current state.</span></span> <span data-ttu-id="ff690-134">Une application effectue cette détermination de manière dynamique après modification de l’état de ligne, généralement due à des activités d’adresse ou d’appel sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="ff690-134">An application would make this determination dynamically after line state changes, typically caused by address or call-related activities on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff690-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff690-135">Requirements</span></span>



| <span data-ttu-id="ff690-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff690-136">Requirement</span></span> | <span data-ttu-id="ff690-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff690-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ff690-138">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ff690-138">TAPI version</span></span><br/> | <span data-ttu-id="ff690-139">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ff690-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ff690-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff690-140">Header</span></span><br/>       | <dl> <span data-ttu-id="ff690-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff690-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff690-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff690-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff690-143">**LINEDEVSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ff690-143">**LINEDEVSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[<span data-ttu-id="ff690-144">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="ff690-144">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="ff690-145">**lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="ff690-145">**lineGetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[<span data-ttu-id="ff690-146">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="ff690-146">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus)
</dt> </dl>

 

 




