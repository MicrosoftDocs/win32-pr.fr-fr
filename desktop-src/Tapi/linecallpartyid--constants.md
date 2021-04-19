---
description: Les \_ constantes d’indicateur de bit LINECALLPARTYID décrivent la nature des informations disponibles sur les parties impliquées dans un appel.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Constantes LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525642"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="e02d9-103">\_Constantes LINECALLPARTYID</span><span class="sxs-lookup"><span data-stu-id="e02d9-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="e02d9-104">Les constantes d’indicateur de bit **LINECALLPARTYID \_** décrivent la nature des informations disponibles sur les parties impliquées dans un appel.</span><span class="sxs-lookup"><span data-stu-id="e02d9-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="e02d9-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**\_adresse LINECALLPARTYID**</span><span class="sxs-lookup"><span data-stu-id="e02d9-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-106">Les informations relatives aux identificateurs de tiers se composent de l’adresse du tiers dans un format d’adresse canonique ou un format d’adresse de numérotation.</span><span class="sxs-lookup"><span data-stu-id="e02d9-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e02d9-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="e02d9-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-108">Les informations de l’identificateur de tiers ne sont pas disponibles, car elles ont été bloquées par le tiers distant.</span><span class="sxs-lookup"><span data-stu-id="e02d9-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e02d9-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**nom de LINECALLPARTYID \_**</span><span class="sxs-lookup"><span data-stu-id="e02d9-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-110">Les informations de l’identificateur de tiers se composent du nom du tiers (par exemple, à partir d’un répertoire conservé à l’intérieur du commutateur).</span><span class="sxs-lookup"><span data-stu-id="e02d9-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e02d9-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**</span><span class="sxs-lookup"><span data-stu-id="e02d9-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-112">Les informations d’ID de l’appelant pour l’appel ne sont pas disponibles, car elles ne sont pas propagées de façon inversée par le réseau.</span><span class="sxs-lookup"><span data-stu-id="e02d9-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e02d9-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ partiel**</span><span class="sxs-lookup"><span data-stu-id="e02d9-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-114">Les informations de l’identificateur de tiers sont valides, mais elles ne sont limitées qu’à des informations partielles.</span><span class="sxs-lookup"><span data-stu-id="e02d9-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e02d9-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="e02d9-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-116">Les informations de l’identificateur de tiers ne sont pas disponibles et ne seront plus disponibles ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e02d9-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="e02d9-117">Les informations peuvent ne pas être disponibles pour des raisons non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e02d9-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="e02d9-118">Par exemple, les informations n’ont pas été remises par le réseau, elles ont été ignorées par le fournisseur de services, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e02d9-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e02d9-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="e02d9-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e02d9-120">Les informations de l’identificateur de tiers sont actuellement inconnues, mais peuvent devenir connues ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="e02d9-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e02d9-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e02d9-121">Remarks</span></span>

<span data-ttu-id="e02d9-122">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="e02d9-122">No extensibility.</span></span> <span data-ttu-id="e02d9-123">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="e02d9-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="e02d9-124">Pour chaque partie possible impliquée dans un appel, les constantes **LINECALLPARTYID \_** décrivent comment les informations de l’identificateur de tiers sont mises en forme.</span><span class="sxs-lookup"><span data-stu-id="e02d9-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="e02d9-125">Ces informations sont fournies dans la structure de données [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="e02d9-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e02d9-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e02d9-126">Requirements</span></span>



| <span data-ttu-id="e02d9-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e02d9-127">Requirement</span></span> | <span data-ttu-id="e02d9-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e02d9-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e02d9-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="e02d9-129">TAPI version</span></span><br/> | <span data-ttu-id="e02d9-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e02d9-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e02d9-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e02d9-131">Header</span></span><br/>       | <dl> <span data-ttu-id="e02d9-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e02d9-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




