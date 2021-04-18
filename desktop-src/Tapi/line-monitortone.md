---
description: Le \_ message MONITORTONE de ligne TAPI est envoyé lorsqu’un ton est détecté. L’envoi de ce message est contrôlé à l’aide de la fonction lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Message LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526447"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="e13f0-104">\_Message MONITORTONE de ligne</span><span class="sxs-lookup"><span data-stu-id="e13f0-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="e13f0-105">Le message **\_ MONITORTONE de ligne** TAPI est envoyé lorsqu’un ton est détecté.</span><span class="sxs-lookup"><span data-stu-id="e13f0-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="e13f0-106">L’envoi de ce message est contrôlé à l’aide de la fonction [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .</span><span class="sxs-lookup"><span data-stu-id="e13f0-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e13f0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e13f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13f0-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="e13f0-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e13f0-109">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="e13f0-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="e13f0-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e13f0-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e13f0-111">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="e13f0-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="e13f0-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e13f0-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e13f0-113">Membre **dwAppSpecific** spécifique à l’application de la structure [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) pour le ton détecté.</span><span class="sxs-lookup"><span data-stu-id="e13f0-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="e13f0-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e13f0-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e13f0-115">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="e13f0-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e13f0-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e13f0-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e13f0-117">« Nombre de cycles » (nombre de millisecondes écoulées depuis le démarrage de Windows) auquel le ton a été détecté.</span><span class="sxs-lookup"><span data-stu-id="e13f0-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="e13f0-118">Pour les versions d’API antérieures à 2,0, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e13f0-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13f0-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e13f0-119">Return value</span></span>

<span data-ttu-id="e13f0-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e13f0-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13f0-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e13f0-121">Remarks</span></span>

<span data-ttu-id="e13f0-122">Le message de **ligne \_ MONITORTONE** est envoyé uniquement à l’application qui a demandé l’analyse du ton.</span><span class="sxs-lookup"><span data-stu-id="e13f0-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="e13f0-123">Étant donné que cet horodateur peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour la comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), **line \_ MONITORTONE**), afin de déterminer leur minutage relatif (séparation entre les événements).</span><span class="sxs-lookup"><span data-stu-id="e13f0-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="e13f0-124">Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="e13f0-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="e13f0-125">Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="e13f0-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13f0-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e13f0-126">Requirements</span></span>



| <span data-ttu-id="e13f0-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e13f0-127">Requirement</span></span> | <span data-ttu-id="e13f0-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e13f0-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e13f0-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="e13f0-129">TAPI version</span></span><br/> | <span data-ttu-id="e13f0-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e13f0-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e13f0-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e13f0-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e13f0-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13f0-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13f0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e13f0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13f0-134">**GATHERDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="e13f0-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="e13f0-135">**générer la ligne \_**</span><span class="sxs-lookup"><span data-stu-id="e13f0-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="e13f0-136">**MONITORDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="e13f0-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="e13f0-137">**LINEMONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="e13f0-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="e13f0-138">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="e13f0-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




