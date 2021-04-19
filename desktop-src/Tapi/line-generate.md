---
description: Le \_ message de génération de la ligne TAPI est envoyé pour notifier l’application que la génération de chiffres ou de tonalités en cours a été arrêtée.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Message LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541653"
---
# <a name="line_generate-message"></a><span data-ttu-id="b09c5-103">Message de génération de ligne \_</span><span class="sxs-lookup"><span data-stu-id="b09c5-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="b09c5-104">Le message **de \_ génération** de la ligne TAPI est envoyé pour notifier l’application que la génération de chiffres ou de tonalités en cours a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="b09c5-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="b09c5-105">Une seule demande de génération de ce type peut être en cours d’exécution d’un appel donné à tout moment.</span><span class="sxs-lookup"><span data-stu-id="b09c5-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="b09c5-106">Ce message est également envoyé lorsque la génération d’un chiffre ou d’un ton est annulée.</span><span class="sxs-lookup"><span data-stu-id="b09c5-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b09c5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b09c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b09c5-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b09c5-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b09c5-109">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b09c5-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="b09c5-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b09c5-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b09c5-111">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="b09c5-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="b09c5-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b09c5-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b09c5-113">Raison pour laquelle la génération de chiffre ou de tonalité a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="b09c5-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="b09c5-114">Ce paramètre doit être une et une seule des [**\_ constantes LINEGENERATETERM**](linegenerateterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b09c5-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b09c5-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b09c5-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b09c5-116">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b09c5-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b09c5-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b09c5-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b09c5-118">« Nombre de cycles » (nombre de millisecondes écoulées depuis le démarrage de Windows) à partir duquel la génération de chiffre ou de tonalité est terminée.</span><span class="sxs-lookup"><span data-stu-id="b09c5-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="b09c5-119">Pour les versions d’API antérieures à 2,0, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="b09c5-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b09c5-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b09c5-120">Return value</span></span>

<span data-ttu-id="b09c5-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b09c5-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b09c5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b09c5-122">Remarks</span></span>

<span data-ttu-id="b09c5-123">Le message de **\_ génération de ligne** est envoyé uniquement à l’application qui a demandé la génération de chiffres ou de tonalités.</span><span class="sxs-lookup"><span data-stu-id="b09c5-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="b09c5-124">Étant donné que l’horodatage spécifié par *dwParam3* peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour effectuer une comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**ligne \_ MONITORDIGITS**](line-monitordigits.md), [**ligne \_ MONITORMEDIA**](line-monitormedia.md), [**ligne \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements).</span><span class="sxs-lookup"><span data-stu-id="b09c5-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="b09c5-125">Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="b09c5-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="b09c5-126">Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="b09c5-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b09c5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b09c5-127">Requirements</span></span>



| <span data-ttu-id="b09c5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b09c5-128">Requirement</span></span> | <span data-ttu-id="b09c5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b09c5-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b09c5-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b09c5-130">TAPI version</span></span><br/> | <span data-ttu-id="b09c5-131">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b09c5-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b09c5-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b09c5-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b09c5-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b09c5-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b09c5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b09c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b09c5-135">**GATHERDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b09c5-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="b09c5-136">**MONITORDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b09c5-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="b09c5-137">**MONITORMEDIA de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b09c5-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="b09c5-138">**MONITORTONE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="b09c5-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




