---
description: Les \_ constantes d’indicateur de bit LINEADDRESSSTATE décrivent les différents éléments d’état d’adresse.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Constantes LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535021"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="5b54b-103">\_Constantes LINEADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="5b54b-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="5b54b-104">Les constantes d’indicateur de bit **LINEADDRESSSTATE \_** décrivent les différents éléments d’état d’adresse.</span><span class="sxs-lookup"><span data-stu-id="5b54b-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="5b54b-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="5b54b-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-106">Indique que, en raison des modifications de configuration apportées par l’utilisateur ou d’autres circonstances, un ou plusieurs membres de la structure [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) pour l’adresse ont changé.</span><span class="sxs-lookup"><span data-stu-id="5b54b-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="5b54b-107">L’application doit utiliser [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) pour lire la structure mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5b54b-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="5b54b-108">Si un fournisseur de services envoie un message [**\_ ADDRESSSTATE de ligne**](line-addressstate.md) contenant cette valeur à TAPI, TAPI le transmet aux applications qui ont négocié TAPI version 1,4 ou ultérieure ; les applications qui négocient une version d’API antérieure recevront les messages de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) qui spécifient LINEDEVSTATE \_ Réinit, en leur demandant d’arrêter et de réinitialiser leur connexion à TAPI pour obtenir les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5b54b-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="5b54b-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-110">L’élément spécifique à l’appareil de l’état de l’adresse a changé.</span><span class="sxs-lookup"><span data-stu-id="5b54b-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE \_ vers l’avant**</span><span class="sxs-lookup"><span data-stu-id="5b54b-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-112">L’état de transfert de l’adresse a changé, y compris éventuellement le nombre d’anneaux pour déterminer une condition de non-réponse.</span><span class="sxs-lookup"><span data-stu-id="5b54b-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="5b54b-113">L’application doit vérifier l’état de l’adresse pour déterminer les détails sur l’état de transfert actuel de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="5b54b-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**</span><span class="sxs-lookup"><span data-stu-id="5b54b-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-115">L’adresse surveillée ou de pont est passée de l’utilisation d’une station à l’utilisation par plusieurs stations.</span><span class="sxs-lookup"><span data-stu-id="5b54b-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**</span><span class="sxs-lookup"><span data-stu-id="5b54b-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-117">L’adresse est passée de inactif ou en cours d’utilisation par de nombreuses stations de pont en cours d’utilisation par une seule station.</span><span class="sxs-lookup"><span data-stu-id="5b54b-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**</span><span class="sxs-lookup"><span data-stu-id="5b54b-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-119">L’adresse est passée à inactif (elle n’est pas utilisée par les stations).</span><span class="sxs-lookup"><span data-stu-id="5b54b-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="5b54b-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-121">Le nombre d’appels sur l’adresse a changé.</span><span class="sxs-lookup"><span data-stu-id="5b54b-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="5b54b-122">Il s’agit du résultat d’événements tels qu’un nouvel appel entrant, d’un appel sortant sur l’adresse ou d’un appel modifiant son état de suspension.</span><span class="sxs-lookup"><span data-stu-id="5b54b-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="5b54b-123">Cet indicateur couvre les modifications apportées à l’un des membres **dwNumActiveCalls**, **dwNumOnHoldCalls** et **dwNumOnHoldPendingCalls** dans la structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="5b54b-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="5b54b-124">L’application doit vérifier les trois membres lorsqu’elle reçoit un message de [**ligne \_ ADDRESSSTATE**](line-addressstate.md) (numCalls).</span><span class="sxs-lookup"><span data-stu-id="5b54b-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ autre**</span><span class="sxs-lookup"><span data-stu-id="5b54b-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-126">Les éléments d’état d’adresse autres que ceux listés ci-dessous ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="5b54b-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="5b54b-127">L’application doit vérifier l’état actuel de l’adresse pour déterminer les éléments qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="5b54b-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5b54b-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminaux LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="5b54b-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5b54b-129">Les paramètres de terminal pour l’adresse ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="5b54b-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b54b-130">Notes</span><span class="sxs-lookup"><span data-stu-id="5b54b-130">Remarks</span></span>

<span data-ttu-id="5b54b-131">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="5b54b-131">No extensibility.</span></span> <span data-ttu-id="5b54b-132">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="5b54b-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="5b54b-133">Une application est avertie des modifications apportées à ces éléments d’État dans le message de [**ligne \_ ADDRESSSTATE**](line-addressstate.md) .</span><span class="sxs-lookup"><span data-stu-id="5b54b-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="5b54b-134">Les fonctionnalités de l’appareil de l’adresse indiquent les modifications d’état d’adresse qui peuvent être signalées pour cette adresse.</span><span class="sxs-lookup"><span data-stu-id="5b54b-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b54b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b54b-135">Requirements</span></span>



| <span data-ttu-id="5b54b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b54b-136">Requirement</span></span> | <span data-ttu-id="5b54b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b54b-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5b54b-138">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="5b54b-138">TAPI version</span></span><br/> | <span data-ttu-id="5b54b-139">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5b54b-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5b54b-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b54b-140">Header</span></span><br/>       | <dl> <span data-ttu-id="5b54b-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b54b-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b54b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b54b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b54b-143">**ADDRESSSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="5b54b-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="5b54b-144">**LINEDEVSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="5b54b-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="5b54b-145">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="5b54b-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="5b54b-146">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="5b54b-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="5b54b-147">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="5b54b-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




