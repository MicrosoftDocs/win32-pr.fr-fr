---
description: Le message d’LINE_MONITORMEDIA TAPI est envoyé lorsqu’une modification du type de média d’appels est détectée. L’envoi de ce message est contrôlé à l’aide de la fonction lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Message LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540449"
---
# <a name="line_monitormedia-message"></a><span data-ttu-id="97066-104">\_Message MONITORMEDIA de ligne</span><span class="sxs-lookup"><span data-stu-id="97066-104">LINE\_MONITORMEDIA message</span></span>

<span data-ttu-id="97066-105">Le message **\_ MONITORMEDIA de ligne** TAPI est envoyé lorsqu’une modification est détectée dans le type de média de l’appel.</span><span class="sxs-lookup"><span data-stu-id="97066-105">The TAPI **LINE\_MONITORMEDIA** message is sent when a change in the call's media type is detected.</span></span> <span data-ttu-id="97066-106">L’envoi de ce message est contrôlé à l’aide de la fonction [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .</span><span class="sxs-lookup"><span data-stu-id="97066-106">The sending of this message is controlled with the [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="97066-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97066-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97066-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="97066-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="97066-109">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="97066-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="97066-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="97066-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="97066-111">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="97066-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="97066-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="97066-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="97066-113">Nouveau type de média (ou mode).</span><span class="sxs-lookup"><span data-stu-id="97066-113">The new media type (or mode).</span></span> <span data-ttu-id="97066-114">Ce paramètre doit être une et une seule des [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="97066-114">This parameter must be one and only one of the [**LINEMEDIAMODE\_ constants**](linemediamode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="97066-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="97066-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="97066-116">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="97066-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="97066-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="97066-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="97066-118">« Nombre de cycles » (nombre de millisecondes écoulées depuis le démarrage de Windows) à partir duquel le média spécifié a été détecté.</span><span class="sxs-lookup"><span data-stu-id="97066-118">The "tick count" (number of milliseconds since Windows started) at which the specified media was detected.</span></span> <span data-ttu-id="97066-119">Pour les versions TAPI antérieures à 2,0, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="97066-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97066-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97066-120">Return value</span></span>

<span data-ttu-id="97066-121">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="97066-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97066-122">Notes</span><span class="sxs-lookup"><span data-stu-id="97066-122">Remarks</span></span>

<span data-ttu-id="97066-123">Le message de **ligne \_ MONITORMEDIA** est envoyé à l’application qui a activé la surveillance du média pour le type de média détecté.</span><span class="sxs-lookup"><span data-stu-id="97066-123">The **LINE\_MONITORMEDIA** message is sent to the application that has enabled media monitoring for the media type detected.</span></span>

<span data-ttu-id="97066-124">Étant donné que cet horodateur peut avoir été généré sur un ordinateur autre que celui sur lequel l’application s’exécute, il est utile uniquement pour la comparaison avec d’autres messages de même horodatage générés sur le même appareil de ligne ( [**ligne \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ generate**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORTONE**](line-monitortone.md)), afin de déterminer leur minutage relatif (séparation entre les événements).</span><span class="sxs-lookup"><span data-stu-id="97066-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="97066-125">Le nombre de cycles peut « habiller » après environ 49,7 jours ; les applications doivent prendre cela en compte lors de l’exécution de calculs.</span><span class="sxs-lookup"><span data-stu-id="97066-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="97066-126">Si le fournisseur de services ne génère pas l’horodateur (par exemple, s’il a été créé à l’aide d’une version antérieure de TAPI), TAPI fournit un horodateur au point le plus proche du fournisseur de services qui génère l’événement afin que l’horodatage synthétisé soit le plus précis possible.</span><span class="sxs-lookup"><span data-stu-id="97066-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="97066-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97066-127">Requirements</span></span>



| <span data-ttu-id="97066-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97066-128">Requirement</span></span> | <span data-ttu-id="97066-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="97066-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97066-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="97066-130">TAPI version</span></span><br/> | <span data-ttu-id="97066-131">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="97066-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="97066-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="97066-132">Header</span></span><br/>       | <dl> <span data-ttu-id="97066-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="97066-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97066-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97066-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97066-135">**GATHERDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="97066-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="97066-136">**générer la ligne \_**</span><span class="sxs-lookup"><span data-stu-id="97066-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="97066-137">**MONITORDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="97066-137">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="97066-138">**MONITORTONE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="97066-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




