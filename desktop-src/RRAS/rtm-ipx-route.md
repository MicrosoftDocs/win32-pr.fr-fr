---
title: Structure de RTM_IPX_ROUTE (RTM. h)
description: La \_ \_ structure d’itinéraires IPX RTM contient des informations qui décrivent un itinéraire pour la famille de protocoles IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE de la structure RAS
- Point d’accès RAS du pointeur de structure PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941903"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="5f604-105">Structure de l' \_ itinéraire IPX RTM \_</span><span class="sxs-lookup"><span data-stu-id="5f604-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="5f604-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5f604-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5f604-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="5f604-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5f604-108">La structure d' **\_ \_ itinéraires IPX RTM** contient des informations qui décrivent un itinéraire pour la famille de protocoles IPX.</span><span class="sxs-lookup"><span data-stu-id="5f604-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f604-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f604-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="5f604-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5f604-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f604-111">**Horodateur du RR \_**</span><span class="sxs-lookup"><span data-stu-id="5f604-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-112">Spécifie l’heure à laquelle l’entrée d’itinéraire a été créée ou mise à jour pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="5f604-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="5f604-113">Ce membre est défini par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="5f604-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="5f604-114">L’heure est exprimée sous la forme d’une structure FILETIME.</span><span class="sxs-lookup"><span data-stu-id="5f604-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="5f604-115">**\_ROUTINGPROTOCOL RR**</span><span class="sxs-lookup"><span data-stu-id="5f604-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-116">Spécifie le protocole de routage qui a ajouté l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="5f604-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="5f604-117">**RR \_ InterfaceId**</span><span class="sxs-lookup"><span data-stu-id="5f604-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-118">Spécifie l’interface par le biais de laquelle l’itinéraire a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="5f604-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="5f604-119">**\_PROTOCOLSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="5f604-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-120">Spécifie une structure de [**\_ \_ données spécifique au protocole**](protocol-specific-data.md) contenant la mémoire réservée pour les données spécifiques aux protocoles de routage.</span><span class="sxs-lookup"><span data-stu-id="5f604-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="5f604-121">**Réseau de RR \_**</span><span class="sxs-lookup"><span data-stu-id="5f604-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-122">Spécifie une structure [**\_ réseau IPX**](ipx-network.md) qui contient une adresse réseau IP.</span><span class="sxs-lookup"><span data-stu-id="5f604-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="5f604-123">**\_NEXTHOPADDRESS RR**</span><span class="sxs-lookup"><span data-stu-id="5f604-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-124">Spécifie une structure d' [**\_ \_ \_ adresse de tronçon suivant IPX**](ipx-next-hop-address.md) qui contient l’adresse du routeur de tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="5f604-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="5f604-125">**\_FAMILYSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="5f604-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="5f604-126">Spécifie une structure de [**\_ \_ données spécifique à IPX**](ipx-specific-data.md) qui contient des données spécifiques à la famille de protocoles IPX.</span><span class="sxs-lookup"><span data-stu-id="5f604-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f604-127">Notes</span><span class="sxs-lookup"><span data-stu-id="5f604-127">Remarks</span></span>

<span data-ttu-id="5f604-128">Les membres de la structure d' **\_ \_ itinéraires IPX RTM** sont tous alignés sur le **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5f604-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f604-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f604-129">Requirements</span></span>



| <span data-ttu-id="5f604-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f604-130">Requirement</span></span> | <span data-ttu-id="5f604-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f604-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5f604-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f604-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5f604-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f604-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="5f604-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f604-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5f604-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f604-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5f604-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5f604-136">End of server support</span></span><br/>    | <span data-ttu-id="5f604-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f604-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="5f604-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f604-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f604-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f604-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f604-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f604-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f604-141">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="5f604-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5f604-142">Structures de la version 1 du gestionnaire de tables de routage \_ \_</span><span class="sxs-lookup"><span data-stu-id="5f604-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="5f604-143">**\_réseau IPX**</span><span class="sxs-lookup"><span data-stu-id="5f604-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="5f604-144">**\_adresse du \_ tronçon \_ suivant IPX**</span><span class="sxs-lookup"><span data-stu-id="5f604-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="5f604-145">**\_données spécifiques à IPX \_**</span><span class="sxs-lookup"><span data-stu-id="5f604-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





