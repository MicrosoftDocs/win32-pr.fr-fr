---
description: Le message de suppression de téléphone TAPI \_ est envoyé pour informer une application de la suppression (suppression du système) d’un appareil téléphonique.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Message PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528518"
---
# <a name="phone_remove-message"></a><span data-ttu-id="02450-103">Message de suppression de téléphone \_</span><span class="sxs-lookup"><span data-stu-id="02450-103">PHONE\_REMOVE message</span></span>

<span data-ttu-id="02450-104">Le message **de \_ Suppression de téléphone** TAPI est envoyé pour informer une application de la suppression (suppression du système) d’un appareil téléphonique.</span><span class="sxs-lookup"><span data-stu-id="02450-104">The TAPI **PHONE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a phone device.</span></span> <span data-ttu-id="02450-105">En général, cela n’est pas utilisé pour les suppressions temporaires, telles que l’extraction d’appareils PCMCIA, mais uniquement pour les suppressions permanentes dans lesquelles l’appareil n’est plus signalé par le fournisseur de services si l’interface TAPI a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="02450-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="02450-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02450-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02450-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="02450-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="02450-108">Réservé.</span><span class="sxs-lookup"><span data-stu-id="02450-108">Reserved.</span></span> <span data-ttu-id="02450-109">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="02450-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="02450-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="02450-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="02450-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="02450-111">Reserved.</span></span> <span data-ttu-id="02450-112">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="02450-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="02450-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="02450-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="02450-114">Identificateur du périphérique téléphonique qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="02450-114">Identifier of the phone device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="02450-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="02450-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="02450-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="02450-116">Reserved.</span></span> <span data-ttu-id="02450-117">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="02450-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="02450-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="02450-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="02450-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="02450-119">Reserved.</span></span> <span data-ttu-id="02450-120">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="02450-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02450-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02450-121">Return value</span></span>

<span data-ttu-id="02450-122">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="02450-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02450-123">Notes</span><span class="sxs-lookup"><span data-stu-id="02450-123">Remarks</span></span>

<span data-ttu-id="02450-124">Les applications TAPI version 2,0 ou ultérieure reçoivent un message de **\_ Suppression de téléphone** .</span><span class="sxs-lookup"><span data-stu-id="02450-124">Applications TAPI version 2.0 or later are sent a **PHONE\_REMOVE** message.</span></span> <span data-ttu-id="02450-125">Cela les informe que l’appareil a été supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="02450-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="02450-126">Le message de **\_ Suppression de téléphone** est précédé d’un message de [**\_ fermeture de téléphone**](phone-close.md) sur chaque descripteur téléphonique, si l’application a ouvert le téléphone.</span><span class="sxs-lookup"><span data-stu-id="02450-126">The **PHONE\_REMOVE** message is preceded by a [**PHONE\_CLOSE**](phone-close.md) message on each phone handle, if the application had the phone open.</span></span> <span data-ttu-id="02450-127">Ce message est envoyé à toutes les applications prenant en charge TAPI version 2,0 ou ultérieure qui ont appelé [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), y compris celles qui n’ont pas d’appareils téléphoniques ouverts à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="02450-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), including those that do not have any phone devices open at the time.</span></span>

<span data-ttu-id="02450-128">Les applications plus anciennes (qui ont négocié la version 1,4 ou une version antérieure) reçoivent un message d' [**\_ État de téléphone**](phone-state.md) spécifiant PHONESTATE \_ supprimé, suivi d’un message de [**\_ fermeture du téléphone**](phone-close.md) .</span><span class="sxs-lookup"><span data-stu-id="02450-128">Older applications (that negotiated TAPI version 1.4 or earlier) are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REMOVED, followed by a [**PHONE\_CLOSE**](phone-close.md) message.</span></span> <span data-ttu-id="02450-129">Contrairement au message de **\_ Suppression de téléphone** , toutefois, ces anciennes applications ne peuvent recevoir ces messages que si elles ont ouvert le téléphone lorsqu’elles sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="02450-129">Unlike the **PHONE\_REMOVE** message, however, these older applications can receive these messages only if they have the phone open when it is removed.</span></span> <span data-ttu-id="02450-130">Si le téléphone n’est pas ouvert, leur seule indication que l’appareil a été supprimé recevrait un \_ NODEVICE PHONEERR lorsqu’il tentera d’accéder à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02450-130">If they do not have the phone open, their only indication that the device was removed would be receiving a PHONEERR\_NODEVICE when they attempt to access the device.</span></span>

<span data-ttu-id="02450-131">Une fois qu’un appareil a été supprimé, toute tentative d’accès à l’appareil par son identificateur d’appareil entraîne une \_ erreur PHONEERR nodevice.</span><span class="sxs-lookup"><span data-stu-id="02450-131">After a device has been removed, any attempt to access the device by its device identifier results in a PHONEERR\_NODEVICE error.</span></span> <span data-ttu-id="02450-132">Une fois que toutes les applications TAPI ont été arrêtées afin que l’interface TAPI puisse redémarrer et, lorsque l’interface TAPI est réinitialisée, l’appareil supprimé n’occupe plus d’identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="02450-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="02450-133">Implémentation : TAPI qui retourne ce \_ message PHONEERR nodevice après \_ réception d’un message de suppression de téléphone d’un fournisseur de services ; aucun autre appel n’est effectué à ce fournisseur de services à l’aide de cet identificateur de périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="02450-133">Implementation: it is TAPI that returns this PHONEERR\_NODEVICE message after a PHONE\_REMOVE message is received from a service provider; no further calls are made to that service provider using that phone device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02450-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02450-134">Requirements</span></span>



| <span data-ttu-id="02450-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02450-135">Requirement</span></span> | <span data-ttu-id="02450-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="02450-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="02450-137">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="02450-137">TAPI version</span></span><br/> | <span data-ttu-id="02450-138">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="02450-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="02450-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="02450-139">Header</span></span><br/>       | <dl> <span data-ttu-id="02450-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="02450-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02450-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02450-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02450-142">**\_Fermer le téléphone**</span><span class="sxs-lookup"><span data-stu-id="02450-142">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="02450-143">**État du téléphone \_**</span><span class="sxs-lookup"><span data-stu-id="02450-143">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="02450-144">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="02450-144">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="02450-145">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="02450-145">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




