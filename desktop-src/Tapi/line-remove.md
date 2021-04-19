---
description: Le message de suppression de ligne TAPI \_ est envoyé pour informer une application de la suppression (suppression du système) d’un périphérique en ligne.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Message LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541149"
---
# <a name="line_remove-message"></a><span data-ttu-id="41b27-103">Message de suppression de ligne \_</span><span class="sxs-lookup"><span data-stu-id="41b27-103">LINE\_REMOVE message</span></span>

<span data-ttu-id="41b27-104">Le message **de \_ Suppression de ligne** TAPI est envoyé pour informer une application de la suppression (suppression du système) d’un périphérique en ligne.</span><span class="sxs-lookup"><span data-stu-id="41b27-104">The TAPI **LINE\_REMOVE** message is sent to inform an application of the removal (deletion from the system) of a line device.</span></span> <span data-ttu-id="41b27-105">En général, cela n’est pas utilisé pour les suppressions temporaires, telles que l’extraction d’appareils PCMCIA, mais uniquement pour les suppressions permanentes dans lesquelles l’appareil n’est plus signalé par le fournisseur de services si l’interface TAPI a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="41b27-105">Generally, this is not used for temporary removals, such as extraction of PCMCIA devices, but only for permanent removals in which the device would no longer be reported by the service provider if TAPI were reinitialized.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="41b27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41b27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b27-107">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="41b27-107">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="41b27-108">Réservé.</span><span class="sxs-lookup"><span data-stu-id="41b27-108">Reserved.</span></span> <span data-ttu-id="41b27-109">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="41b27-109">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="41b27-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="41b27-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="41b27-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="41b27-111">Reserved.</span></span> <span data-ttu-id="41b27-112">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="41b27-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="41b27-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="41b27-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="41b27-114">Identificateur du périphérique de ligne qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="41b27-114">Identifier of the line device that was removed.</span></span>

</dd> <dt>

<span data-ttu-id="41b27-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="41b27-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="41b27-116">Réservé.</span><span class="sxs-lookup"><span data-stu-id="41b27-116">Reserved.</span></span> <span data-ttu-id="41b27-117">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="41b27-117">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="41b27-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="41b27-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="41b27-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="41b27-119">Reserved.</span></span> <span data-ttu-id="41b27-120">Définit la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="41b27-120">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b27-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41b27-121">Return value</span></span>

<span data-ttu-id="41b27-122">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="41b27-122">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41b27-123">Notes</span><span class="sxs-lookup"><span data-stu-id="41b27-123">Remarks</span></span>

<span data-ttu-id="41b27-124">Les applications prenant en charge TAPI version 2,0 ou ultérieure reçoivent un message de **\_ Suppression de ligne** .</span><span class="sxs-lookup"><span data-stu-id="41b27-124">Applications supporting TAPI version 2.0 or later are sent a **LINE\_REMOVE** message.</span></span> <span data-ttu-id="41b27-125">Cela les informe que l’appareil a été supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="41b27-125">This informs them that the device has been removed from the system.</span></span> <span data-ttu-id="41b27-126">Le message de **\_ Suppression de ligne** est précédé d’un message de [**\_ fermeture de ligne**](line-close.md) sur chaque handle de ligne, si la ligne est ouverte dans l’application.</span><span class="sxs-lookup"><span data-stu-id="41b27-126">The **LINE\_REMOVE** message is preceded by a [**LINE\_CLOSE**](line-close.md) message on each line handle, if the application had the line open.</span></span> <span data-ttu-id="41b27-127">Ce message est envoyé à toutes les applications prenant en charge TAPI version 2,0 ou ultérieure, appelées [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), y compris celles qui n’ont pas d’appareils de ligne ouverts à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="41b27-127">This message is sent to all applications supporting TAPI version 2.0 or later that have called [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

<span data-ttu-id="41b27-128">Les applications plus anciennes reçoivent un message de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) en spécifiant LINEDEVSTATE \_ supprimé, suivi d’un message de fermeture de ligne \_ .</span><span class="sxs-lookup"><span data-stu-id="41b27-128">Older applications are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REMOVED, followed by a LINE\_CLOSE message.</span></span> <span data-ttu-id="41b27-129">Toutefois, contrairement au message de **\_ Suppression de ligne** , ces anciennes applications ne peuvent recevoir ces messages que si la ligne est ouverte lorsqu’elle est supprimée.</span><span class="sxs-lookup"><span data-stu-id="41b27-129">Unlike the **LINE\_REMOVE** message, however, these older applications can receive these messages only if they have the line open when it is removed.</span></span> <span data-ttu-id="41b27-130">S’ils n’ont pas de ligne ouverte, leur seule indication que l’appareil a été supprimé recevrait une \_ erreur LINEERR nodevice lorsqu’ils tenteront d’accéder à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="41b27-130">If they do not have the line open, their only indication that the device was removed would be receiving a LINEERR\_NODEVICE error when they attempt to access the device.</span></span>

<span data-ttu-id="41b27-131">Une fois qu’un appareil a été supprimé, toute tentative d’accès à l’appareil par son identificateur d’appareil entraîne une \_ erreur LINEERR nodevice.</span><span class="sxs-lookup"><span data-stu-id="41b27-131">After a device has been removed, any attempt to access the device by its device identifier results in a LINEERR\_NODEVICE error.</span></span> <span data-ttu-id="41b27-132">Une fois que toutes les applications TAPI ont été arrêtées afin que l’interface TAPI puisse redémarrer et, lorsque l’interface TAPI est réinitialisée, l’appareil supprimé n’occupe plus d’identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="41b27-132">After all TAPI applications have shutdown so that TAPI can restart, and when TAPI is reinitialized, the removed device no longer occupies a device identifier.</span></span>

> [!Note]  
> <span data-ttu-id="41b27-133">Implémentation : il s’agit de l’interface TAPI qui retourne ce LINEERR \_ nodevice ; après réception d’un message de **\_ Suppression de ligne** d’un fournisseur de services, aucun autre appel n’est effectué à ce fournisseur de services à l’aide de cet identificateur de périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="41b27-133">Implementation: it is TAPI that returns this LINEERR\_NODEVICE; after a **LINE\_REMOVE** message is received from a service provider; no further calls are made to that service provider using that line device identifier.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41b27-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41b27-134">Requirements</span></span>



| <span data-ttu-id="41b27-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41b27-135">Requirement</span></span> | <span data-ttu-id="41b27-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="41b27-136">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="41b27-137">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="41b27-137">TAPI version</span></span><br/> | <span data-ttu-id="41b27-138">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="41b27-138">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="41b27-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="41b27-139">Header</span></span><br/>       | <dl> <span data-ttu-id="41b27-140"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="41b27-140"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b27-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41b27-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b27-142">**fermeture de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="41b27-142">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="41b27-143">**LINEDEVSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="41b27-143">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="41b27-144">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="41b27-144">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




