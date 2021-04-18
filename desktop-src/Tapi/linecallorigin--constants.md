---
description: Les \_ constantes LINECALLORIGIN décrivent l’origine d’un appel.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Constantes LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532819"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="17600-103">\_Constantes LINECALLORIGIN</span><span class="sxs-lookup"><span data-stu-id="17600-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="17600-104">Les constantes **LINECALLORIGIN \_** décrivent l’origine d’un appel.</span><span class="sxs-lookup"><span data-stu-id="17600-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="17600-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_Conférence LINECALLORIGIN**</span><span class="sxs-lookup"><span data-stu-id="17600-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-106">Le descripteur d’appel est destiné à un appel de conférence, autrement dit, il s’agit de la connexion de l’application au pont de conférence dans le commutateur.</span><span class="sxs-lookup"><span data-stu-id="17600-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17600-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ externe**</span><span class="sxs-lookup"><span data-stu-id="17600-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-108">L’appel est issu d’un appel entrant sur une ligne externe.</span><span class="sxs-lookup"><span data-stu-id="17600-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17600-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN \_ entrant**</span><span class="sxs-lookup"><span data-stu-id="17600-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-110">L’appel est issu d’un appel entrant, mais le fournisseur de services ne peut pas déterminer s’il provient d’une autre station sur le même commutateur ou à partir d’une ligne externe.</span><span class="sxs-lookup"><span data-stu-id="17600-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="17600-111">Les fournisseurs de services peuvent utiliser cette constante uniquement lorsque TAPI version 1,4 ou ultérieure a été négocié.</span><span class="sxs-lookup"><span data-stu-id="17600-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="17600-112">Dans le cas contraire, le fournisseur de services peut substituer LINECALLORIGIN \_ .</span><span class="sxs-lookup"><span data-stu-id="17600-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17600-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interne**</span><span class="sxs-lookup"><span data-stu-id="17600-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-114">L’appel est issu d’un appel entrant au niveau d’une station interne au même environnement de basculement.</span><span class="sxs-lookup"><span data-stu-id="17600-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17600-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN \_ sortant**</span><span class="sxs-lookup"><span data-stu-id="17600-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-116">L’appel provient de cette station en tant qu’appel sortant.</span><span class="sxs-lookup"><span data-stu-id="17600-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17600-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN \_ INdispo**</span><span class="sxs-lookup"><span data-stu-id="17600-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-118">L’origine de l’appel n’est pas disponible et ne sera jamais connue pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="17600-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17600-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="17600-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17600-120">L’origine de l’appel est actuellement inconnue, mais peut devenir connue ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="17600-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17600-121">Notes</span><span class="sxs-lookup"><span data-stu-id="17600-121">Remarks</span></span>

<span data-ttu-id="17600-122">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="17600-122">No extensibility.</span></span> <span data-ttu-id="17600-123">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="17600-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="17600-124">L’origine d’un appel est stockée dans le membre **dwOrigin** de la structure [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) de l’appel.</span><span class="sxs-lookup"><span data-stu-id="17600-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="17600-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17600-125">Requirements</span></span>



| <span data-ttu-id="17600-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17600-126">Requirement</span></span> | <span data-ttu-id="17600-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="17600-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="17600-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="17600-128">TAPI version</span></span><br/> | <span data-ttu-id="17600-129">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="17600-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="17600-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="17600-130">Header</span></span><br/>       | <dl> <span data-ttu-id="17600-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="17600-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




