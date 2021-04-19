---
description: Le \_ message MONITORDIGITS de ligne TAPI est envoyé lors de la détection d’un chiffre. L’envoi de ce message est contrôlé à l’aide de la fonction lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Message LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523622"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="b0b5f-104">\_Message MONITORDIGITS de ligne</span><span class="sxs-lookup"><span data-stu-id="b0b5f-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="b0b5f-105">Le message **\_ MONITORDIGITS de ligne** TAPI est envoyé lors de la détection d’un chiffre.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="b0b5f-106">L’envoi de ce message est contrôlé à l’aide de la fonction [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .</span><span class="sxs-lookup"><span data-stu-id="b0b5f-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b0b5f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0b5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0b5f-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b0b5f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b5f-109">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="b0b5f-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b0b5f-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b5f-111">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="b0b5f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b0b5f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b5f-113">L’octet de poids faible contient le dernier chiffre reçu dans une représentation textuelle.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="b0b5f-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b0b5f-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b5f-115">Mode de chiffrement détecté.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-115">The digit mode that was detected.</span></span> <span data-ttu-id="b0b5f-116">Ce paramètre doit être une et une seule des [**\_ constantes LINEDIGITMODE**](linedigitmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b0b5f-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0b5f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b0b5f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b0b5f-118">« Tick Count » (nombre de millisecondes écoulées depuis le début de Windows) à partir duquel le chiffre spécifié a été détecté.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="b0b5f-119">Pour les versions TAPI antérieures à 2,0, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0b5f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0b5f-120">Return value</span></span>

<span data-ttu-id="b0b5f-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b5f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b0b5f-122">Remarks</span></span>

<span data-ttu-id="b0b5f-123">Le message de **ligne \_ MONITORDIGITS** est envoyé à l’application qui a activé la surveillance des chiffres.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="b0b5f-124">Étant donné que cet horodateur peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour la comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements).</span><span class="sxs-lookup"><span data-stu-id="b0b5f-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="b0b5f-125">Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="b0b5f-126">Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="b0b5f-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b5f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0b5f-127">Requirements</span></span>



| <span data-ttu-id="b0b5f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b5f-128">Requirement</span></span> | <span data-ttu-id="b0b5f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b5f-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b0b5f-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b0b5f-130">TAPI version</span></span><br/> | <span data-ttu-id="b0b5f-131">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b0b5f-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b0b5f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0b5f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b0b5f-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5f-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b5f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0b5f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b5f-135">**GATHERDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b0b5f-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="b0b5f-136">**générer la ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b0b5f-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="b0b5f-137">**MONITORMEDIA de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b0b5f-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="b0b5f-138">**MONITORTONE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b0b5f-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="b0b5f-139">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="b0b5f-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




