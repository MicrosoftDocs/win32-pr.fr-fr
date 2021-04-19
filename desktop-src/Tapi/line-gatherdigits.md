---
description: Le message GATHERDIGITS de ligne TAPI \_ est envoyé lorsque la demande de collecte de chiffres mise en mémoire tampon est terminée ou annulée. La mémoire tampon de chiffres peut être examinée une fois que le message a été reçu par l’application.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Message LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535965"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="eb018-104">\_Message GATHERDIGITS de ligne</span><span class="sxs-lookup"><span data-stu-id="eb018-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="eb018-105">Le message **\_ GATHERDIGITS de ligne** TAPI est envoyé lorsque la demande de collecte de chiffres mise en mémoire tampon est terminée ou annulée.</span><span class="sxs-lookup"><span data-stu-id="eb018-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="eb018-106">La mémoire tampon de chiffres peut être examinée une fois que le message a été reçu par l’application.</span><span class="sxs-lookup"><span data-stu-id="eb018-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="eb018-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb018-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb018-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="eb018-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="eb018-109">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="eb018-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="eb018-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="eb018-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="eb018-111">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="eb018-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="eb018-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="eb018-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="eb018-113">Raison pour laquelle la collecte de chiffres s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="eb018-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="eb018-114">Ce paramètre doit être une et une seule des [**\_ constantes LINEGATHERTERM**](linegatherterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="eb018-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb018-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="eb018-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="eb018-116">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="eb018-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="eb018-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="eb018-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="eb018-118">« Nombre de cycles » (nombre de millisecondes écoulées depuis le démarrage de Windows) à partir duquel la collecte des chiffres est terminée.</span><span class="sxs-lookup"><span data-stu-id="eb018-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="eb018-119">Pour les versions TAPI antérieures à 2,0, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="eb018-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb018-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb018-120">Return value</span></span>

<span data-ttu-id="eb018-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="eb018-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb018-122">Notes</span><span class="sxs-lookup"><span data-stu-id="eb018-122">Remarks</span></span>

<span data-ttu-id="eb018-123">Le message de **ligne \_ GATHERDIGITS** est envoyé à l’application qui a initié la collecte des chiffres sur l’appel à l’aide de [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span><span class="sxs-lookup"><span data-stu-id="eb018-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="eb018-124">Si la fonction [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) est utilisée pour annuler une requête précédente en vue de recueillir des chiffres, TAPI envoie un message de **ligne \_ GATHERDIGITS** avec *dwParam1* défini sur LINEGATHERTERM \_ Cancel à l’application, indiquant que la mémoire tampon spécifiée à l’origine contient les chiffres regroupés jusqu’à l’annulation.</span><span class="sxs-lookup"><span data-stu-id="eb018-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="eb018-125">Étant donné que l’horodatage spécifié par *dwParam3* peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour effectuer une comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements).</span><span class="sxs-lookup"><span data-stu-id="eb018-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="eb018-126">Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="eb018-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="eb018-127">Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="eb018-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="eb018-128">Lorsqu’une application appelle une opération asynchrone qui écrit des données dans la mémoire de l’application, l’application doit conserver cette mémoire disponible pour l’écriture jusqu’à la réception d’un message de [**\_ réponse**](line-reply.md) de ligne ou de **\_ GATHERDIGITS de ligne** .</span><span class="sxs-lookup"><span data-stu-id="eb018-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb018-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb018-129">Requirements</span></span>



| <span data-ttu-id="eb018-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb018-130">Requirement</span></span> | <span data-ttu-id="eb018-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb018-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="eb018-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="eb018-132">TAPI version</span></span><br/> | <span data-ttu-id="eb018-133">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="eb018-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="eb018-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb018-134">Header</span></span><br/>       | <dl> <span data-ttu-id="eb018-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb018-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb018-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb018-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb018-137">**générer la ligne \_**</span><span class="sxs-lookup"><span data-stu-id="eb018-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="eb018-138">**MONITORDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="eb018-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="eb018-139">**MONITORMEDIA de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="eb018-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="eb018-140">**MONITORTONE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="eb018-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="eb018-141">**réponse de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="eb018-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="eb018-142">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="eb018-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




