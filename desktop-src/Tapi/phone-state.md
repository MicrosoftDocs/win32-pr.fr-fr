---
description: L’interface TAPI envoie le \_ message d’État téléphonique à une application chaque fois que l’état d’un périphérique téléphonique change.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Message PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538576"
---
# <a name="phone_state-message"></a><span data-ttu-id="4302e-103">Message d’état de téléphone \_</span><span class="sxs-lookup"><span data-stu-id="4302e-103">PHONE\_STATE message</span></span>

<span data-ttu-id="4302e-104">L’interface TAPI envoie le message d' **\_ État téléphonique** à une application chaque fois que l’état d’un périphérique téléphonique change.</span><span class="sxs-lookup"><span data-stu-id="4302e-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="4302e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4302e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4302e-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="4302e-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="4302e-107">Handle vers l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="4302e-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="4302e-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="4302e-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4302e-109">Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="4302e-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="4302e-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4302e-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4302e-111">État du téléphone qui a changé.</span><span class="sxs-lookup"><span data-stu-id="4302e-111">The phone state that has changed.</span></span> <span data-ttu-id="4302e-112">Ce paramètre utilise l’une des [**\_ constantes PHONESTATE**](phonestate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="4302e-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4302e-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4302e-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4302e-114">Les informations dépendantes de l’état du téléphone détaillent le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="4302e-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="4302e-115">Ce paramètre n’est pas utilisé si plusieurs indicateurs sont définis dans *dwParam1*, car plusieurs éléments d’État ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="4302e-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="4302e-116">L’application doit appeler [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) pour obtenir un ensemble complet d’informations.</span><span class="sxs-lookup"><span data-stu-id="4302e-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="4302e-117">Si *dwParam1* est PHONESTATE \_ Owner, *dwParam2* contient le nouveau nombre de propriétaires.</span><span class="sxs-lookup"><span data-stu-id="4302e-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="4302e-118">Si *dwParam1* est PHONESTATE \_ Monitors, *dwParam2* contient le nouveau nombre d’analyses.</span><span class="sxs-lookup"><span data-stu-id="4302e-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="4302e-119">Si *dwParam1* est PHONESTATE \_ LAMP, *dwParam2* contient l’identificateur de bouton/lampe de la lampe qui a changé.</span><span class="sxs-lookup"><span data-stu-id="4302e-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="4302e-120">Si *dwParam1* est PHONESTATE \_ RINGMODE, *dwParam2* contient le nouveau mode Ring.</span><span class="sxs-lookup"><span data-stu-id="4302e-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="4302e-121">Si *dwParam1* est PHONESTATE \_ combiné, haut-parleur ou casque, *dwParam2* contient le nouveau mode hookswitch de cet appareil hookswitch.</span><span class="sxs-lookup"><span data-stu-id="4302e-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="4302e-122">Ce paramètre utilise l’une des [**\_ constantes PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="4302e-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4302e-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4302e-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4302e-124">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="4302e-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4302e-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4302e-125">Return value</span></span>

<span data-ttu-id="4302e-126">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="4302e-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4302e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="4302e-127">Remarks</span></span>

<span data-ttu-id="4302e-128">L’envoi du message d' **\_ État téléphonique** à l’application peut être contrôlé et interrogé à l’aide de [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) et [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="4302e-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="4302e-129">Par défaut, ce message est désactivé pour toutes les modifications d’État, à l’exception de PHONESTATE \_ reinit, qui ne peut pas être désactivé.</span><span class="sxs-lookup"><span data-stu-id="4302e-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="4302e-130">Ce message est envoyé à toutes les applications qui ont un handle vers le téléphone, y compris celles qui ont appelé [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) avec le paramètre *DWPRIVILEGES* défini sur PHONEPRIVILEGE \_ owner ou PHONEPRIVILEGE \_ Monitor.</span><span class="sxs-lookup"><span data-stu-id="4302e-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="4302e-131">Un message d' **\_ État de téléphone** avec un propriétaire et/ou une indication d’analyse est envoyé aux applications qui ont déjà un handle pour le téléphone.</span><span class="sxs-lookup"><span data-stu-id="4302e-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="4302e-132">Cela peut être le résultat d’une autre application modifiant la propriété ou la surveillance du périphérique téléphonique avec [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) ou [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span><span class="sxs-lookup"><span data-stu-id="4302e-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="4302e-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4302e-133">Requirements</span></span>



| <span data-ttu-id="4302e-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4302e-134">Requirement</span></span> | <span data-ttu-id="4302e-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="4302e-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4302e-136">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="4302e-136">TAPI version</span></span><br/> | <span data-ttu-id="4302e-137">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4302e-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4302e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4302e-138">Header</span></span><br/>       | <dl> <span data-ttu-id="4302e-139"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4302e-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4302e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4302e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4302e-141">**\_Fermer le téléphone**</span><span class="sxs-lookup"><span data-stu-id="4302e-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="4302e-142">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="4302e-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="4302e-143">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="4302e-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="4302e-144">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="4302e-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="4302e-145">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="4302e-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="4302e-146">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="4302e-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="4302e-147">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="4302e-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="4302e-148">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="4302e-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="4302e-149">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="4302e-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="4302e-150">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="4302e-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="4302e-151">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="4302e-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




