---
description: Les \_ constantes d’indicateur de bit LINEOFFERINGMODE (TAPI versions 1,4 et ultérieures) décrivent différents sous-États d’un appel d’offre.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Constantes LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535324"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="d2720-103">\_Constantes LINEOFFERINGMODE</span><span class="sxs-lookup"><span data-stu-id="d2720-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="d2720-104">Les constantes d’indicateur de bit **LINEOFFERINGMODE \_** (TAPI versions 1,4 et ultérieures) décrivent différents sous-États d’un appel d’offre.</span><span class="sxs-lookup"><span data-stu-id="d2720-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="d2720-105">Un mode est disponible en tant qu’État d’appel à l’application après l’état d’appel trdansitions à l’offre, et dans le message de [**ligne \_ CALLSTATE**](line-callstate.md) indiquant que l’appel se trouve dans l' \_ offre LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="d2720-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="d2720-106">Ces valeurs sont utilisées lorsque l’appel est sur une adresse partagée (Bridged) avec d’autres stations (voir [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique.</span><span class="sxs-lookup"><span data-stu-id="d2720-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="d2720-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ actif**</span><span class="sxs-lookup"><span data-stu-id="d2720-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d2720-108">Indique que l’appel est en cours d’alerte au niveau de la station active (est accompagné des \_ messages de sonnerie LINEDEVSTATE) et, si une application est configurée pour répondre automatiquement, elle peut le faire.</span><span class="sxs-lookup"><span data-stu-id="d2720-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="d2720-109">Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est active (ce qui serait la situation sur une adresse sans pont).</span><span class="sxs-lookup"><span data-stu-id="d2720-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="d2720-110">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="d2720-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2720-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ inactif**</span><span class="sxs-lookup"><span data-stu-id="d2720-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d2720-112">Indique que l’appel est proposé sur plusieurs stations, mais que la station actuelle ne fait pas l’objet d’une alerte (par exemple, il peut s’agir d’une station de surveillance dans laquelle l’état de l’offre est un avis, tel que le clignotement d’une lumière); les logiciels de la station définie pour la réponse automatique doivent de préférence ne pas répondre à l’appel, car il doit s’agir de la prérogative au niveau de la station principale (alerte), mais [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) peut être utilisé pour connecter l’appel.</span><span class="sxs-lookup"><span data-stu-id="d2720-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="d2720-113">(TAPI versions 1,4 et ultérieures)</span><span class="sxs-lookup"><span data-stu-id="d2720-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2720-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d2720-114">Remarks</span></span>

<span data-ttu-id="d2720-115">Non extensible.</span><span class="sxs-lookup"><span data-stu-id="d2720-115">Not extensible.</span></span> <span data-ttu-id="d2720-116">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="d2720-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="d2720-117">Pour la compatibilité descendante, il incombe au fournisseur de services d’examiner la version de l’API négociée sur la ligne et de ne pas utiliser ces \_ valeurs LINEOFFERINGMODE si elles ne sont pas prises en charge sur la version négociée.</span><span class="sxs-lookup"><span data-stu-id="d2720-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="d2720-118">Les applications qui ne sont pas Cognizant de LINEOFFERINGMODE \_ supposent probablement qu’un appel qui est dans l' \_ offre LINECALLSTATE est dans LINEOFFERINGMODE \_ actif.</span><span class="sxs-lookup"><span data-stu-id="d2720-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="d2720-119">Les \_ \_ valeurs inactives LINEOFFERINGMODE actives et LINEOFFERINGMODE sont utilisées lorsque l’appel est sur une adresse partagée avec d’autres stations (Bridged, voir [ \_ constantes LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalement des systèmes à clé électronique.</span><span class="sxs-lookup"><span data-stu-id="d2720-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="d2720-120">Si le mode d’état d’appel de l’offre est « actif », cela signifie que l’appel est en cours d’alerte au niveau de la station active (est accompagné de \_ messages de sonnerie LINEDEVSTATE), et si une application est configurée pour répondre automatiquement, elle peut le faire.</span><span class="sxs-lookup"><span data-stu-id="d2720-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="d2720-121">Si le mode d’état de l’appel est « inactif », l’appel est proposé sur plusieurs stations, mais la station actuelle ne fait pas l’objet d’une alerte (par exemple, il peut s’agir d’une station de surveillance dans laquelle l’état de l’offre est un avis, tel que le clignotement d’une lumière); les logiciels de la station définie pour la réponse automatique doivent de préférence ne pas répondre à l’appel, car il doit s’agir de la prérogative au niveau de la station principale (alerte), mais [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) peut être utilisé pour connecter l’appel.</span><span class="sxs-lookup"><span data-stu-id="d2720-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="d2720-122">Si le mode d’état de l’appel est égal à zéro, l’application doit supposer que la valeur est active (ce qui serait la situation sur une adresse sans pont).</span><span class="sxs-lookup"><span data-stu-id="d2720-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2720-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2720-123">Requirements</span></span>



| <span data-ttu-id="d2720-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2720-124">Requirement</span></span> | <span data-ttu-id="d2720-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2720-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d2720-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d2720-126">TAPI version</span></span><br/> | <span data-ttu-id="d2720-127">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d2720-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d2720-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2720-128">Header</span></span><br/>       | <dl> <span data-ttu-id="d2720-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2720-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




