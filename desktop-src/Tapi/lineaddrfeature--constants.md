---
description: Les \_ constantes LINEADDRFEATURE répertorient les opérations qui peuvent être appelées sur une adresse.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Constantes LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539673"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="5becc-103">\_Constantes LINEADDRFEATURE</span><span class="sxs-lookup"><span data-stu-id="5becc-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="5becc-104">Les constantes **LINEADDRFEATURE \_** répertorient les opérations qui peuvent être appelées sur une adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="5becc-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ vers l’avant**</span><span class="sxs-lookup"><span data-stu-id="5becc-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-106">L’adresse peut être transférée.</span><span class="sxs-lookup"><span data-stu-id="5becc-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="5becc-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-108">Un appel sortant peut être placé sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**\_collecte LINEADDRFEATURE**</span><span class="sxs-lookup"><span data-stu-id="5becc-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-110">Un appel peut être récupéré à l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**</span><span class="sxs-lookup"><span data-stu-id="5becc-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-112">La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut être utilisée pour récupérer un appel sur une adresse spécifique.</span><span class="sxs-lookup"><span data-stu-id="5becc-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**</span><span class="sxs-lookup"><span data-stu-id="5becc-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-114">La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut être utilisée pour récupérer un appel dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="5becc-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**</span><span class="sxs-lookup"><span data-stu-id="5becc-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-116">La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (avec une adresse de destination **null** ) peut être utilisée pour récupérer un appel détenu sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="5becc-117">Cela est normalement utilisé uniquement dans une organisation avec pontage exclusive.</span><span class="sxs-lookup"><span data-stu-id="5becc-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**</span><span class="sxs-lookup"><span data-stu-id="5becc-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-119">La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (avec une adresse de destination **null** ) peut être utilisée pour récupérer un appel d’appel en attente.</span><span class="sxs-lookup"><span data-stu-id="5becc-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="5becc-120">Notez que cela n’indique pas nécessairement qu’un appel en attente est réellement présent, car il est souvent impossible pour un appareil de téléphonie de détecter automatiquement un tel appel ; Toutefois, il indique que la fonction de raccordement-Flash sera appelée pour tenter de basculer vers ce type d’appel.</span><span class="sxs-lookup"><span data-stu-id="5becc-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="5becc-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-122">Le contrôle de média peut être défini sur cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**</span><span class="sxs-lookup"><span data-stu-id="5becc-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-124">Les modes de terminal pour cette adresse peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="5becc-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**</span><span class="sxs-lookup"><span data-stu-id="5becc-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-126">Un appel de conférence avec un appel initial **null** peut être configuré à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**</span><span class="sxs-lookup"><span data-stu-id="5becc-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-128">Les demandes d’achèvement d’appel peuvent être annulées à cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**déspark LINEADDRFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="5becc-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-130">Les appels peuvent être désimmobilisés à l’aide de cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="5becc-131">Si aucun des nouveaux bits modifiés « PICKUP » n’est défini dans le membre **dwAddressFeatures** dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mais que le \_ bit de collecte LINEADDRFEATURE est défini, alors l’un des modes de collecte peut fonctionner ; le fournisseur de services n’a simplement pas spécifié les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="5becc-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="5becc-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-133">La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (avec une adresse de destination vide) peut être utilisée pour activer la fonctionnalité ne pas déranger sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="5becc-134">LINEADDRFEATURE \_ Forward sera également défini.</span><span class="sxs-lookup"><span data-stu-id="5becc-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5becc-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="5becc-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5becc-136">La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) peut être utilisée pour transférer des appels sur l’adresse à d’autres nombres.</span><span class="sxs-lookup"><span data-stu-id="5becc-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="5becc-137">LINEADDRFEATURE \_ Forward sera également défini.</span><span class="sxs-lookup"><span data-stu-id="5becc-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="5becc-138">Si aucun des nouveaux bits « FORWARD » modifiés n’est défini dans le membre **dwAddressFeatures** dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mais que le \_ bit de transfert LINEADDRFEATURE est défini, alors l’un des modes de transfert peut fonctionner ; le fournisseur de services n’a simplement pas spécifié les uns des autres.</span><span class="sxs-lookup"><span data-stu-id="5becc-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5becc-139">Notes</span><span class="sxs-lookup"><span data-stu-id="5becc-139">Remarks</span></span>

<span data-ttu-id="5becc-140">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="5becc-140">No extensibility.</span></span> <span data-ttu-id="5becc-141">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="5becc-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="5becc-142">Cette constante est utilisée à la fois dans [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (retournée par [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) et dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (retournée par [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span><span class="sxs-lookup"><span data-stu-id="5becc-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="5becc-143">**LINEADDRESSCAPS** signale la disponibilité des fonctionnalités d’adresse par le fournisseur de services (principalement le commutateur) pour une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="5becc-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="5becc-144">Une application effectue cette détermination lors de son initialisation.</span><span class="sxs-lookup"><span data-stu-id="5becc-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="5becc-145">La structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) signale, pour une adresse donnée, les fonctionnalités d’adresse qui peuvent être appelées alors que l’adresse est dans l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="5becc-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="5becc-146">Une application effectue cette détermination de manière dynamique après modification de l’état de l’adresse, généralement provoquée par les activités liées aux appels sur l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5becc-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="5becc-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5becc-147">Requirements</span></span>



| <span data-ttu-id="5becc-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5becc-148">Requirement</span></span> | <span data-ttu-id="5becc-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="5becc-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5becc-150">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5becc-150">TAPI version</span></span><br/> | <span data-ttu-id="5becc-151">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5becc-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5becc-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="5becc-152">Header</span></span><br/>       | <dl> <span data-ttu-id="5becc-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5becc-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5becc-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5becc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5becc-155">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="5becc-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="5becc-156">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="5becc-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="5becc-157">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="5becc-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="5becc-158">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="5becc-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="5becc-159">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="5becc-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="5becc-160">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="5becc-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




