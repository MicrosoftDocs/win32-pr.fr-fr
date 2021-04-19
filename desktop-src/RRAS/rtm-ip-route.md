---
title: Structure de RTM_IP_ROUTE (RTM. h)
description: La structure de l' \_ itinéraire IP RTM \_ contient des informations qui décrivent un itinéraire appartenant à la famille de protocoles IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE de la structure RAS
- Point d’accès RAS du pointeur de structure PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516502"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="3310e-105">Structure de l' \_ itinéraire IP RTM \_</span><span class="sxs-lookup"><span data-stu-id="3310e-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="3310e-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3310e-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="3310e-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="3310e-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="3310e-108">La structure de l' **\_ \_ itinéraire IP RTM** contient des informations qui décrivent un itinéraire appartenant à la famille de protocoles IP.</span><span class="sxs-lookup"><span data-stu-id="3310e-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="3310e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3310e-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="3310e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="3310e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="3310e-111">**Horodateur du RR \_**</span><span class="sxs-lookup"><span data-stu-id="3310e-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-112">Spécifie l’heure à laquelle l’entrée d’itinéraire a été créée ou mise à jour pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="3310e-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="3310e-113">Ce membre est défini par le gestionnaire de tables de routage.</span><span class="sxs-lookup"><span data-stu-id="3310e-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="3310e-114">L’heure est exprimée sous la forme d’une structure FILETIME.</span><span class="sxs-lookup"><span data-stu-id="3310e-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="3310e-115">**\_ROUTINGPROTOCOL RR**</span><span class="sxs-lookup"><span data-stu-id="3310e-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-116">Spécifie le protocole de routage qui a ajouté l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="3310e-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="3310e-117">**RR \_ InterfaceId**</span><span class="sxs-lookup"><span data-stu-id="3310e-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-118">Spécifie l’interface par le biais de laquelle l’itinéraire a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="3310e-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="3310e-119">**\_PROTOCOLSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="3310e-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-120">Spécifie une structure de [**\_ \_ données spécifique au protocole**](protocol-specific-data.md) qui contient la mémoire réservée pour les données spécifiques au protocole de routage.</span><span class="sxs-lookup"><span data-stu-id="3310e-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="3310e-121">**Réseau de RR \_**</span><span class="sxs-lookup"><span data-stu-id="3310e-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-122">Spécifie une structure de [**\_ réseau IP**](ip-network.md) qui contient une adresse réseau IP.</span><span class="sxs-lookup"><span data-stu-id="3310e-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="3310e-123">**\_NEXTHOPADDRESS RR**</span><span class="sxs-lookup"><span data-stu-id="3310e-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-124">Spécifie une structure d' [**adresse IP de \_ \_ saut \_ suivant**](ip-next-hop-address.md) qui contient l’adresse du routeur de tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="3310e-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="3310e-125">**\_FAMILYSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="3310e-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="3310e-126">Spécifie une structure de [**\_ \_ données spécifique à l’adresse IP**](ip-specific-data.md) qui contient des données spécifiques à la famille de protocoles IP.</span><span class="sxs-lookup"><span data-stu-id="3310e-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3310e-127">Notes</span><span class="sxs-lookup"><span data-stu-id="3310e-127">Remarks</span></span>

<span data-ttu-id="3310e-128">Les membres de la structure d' **\_ \_ itinéraires IP RTM** sont tous alignés sur le **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3310e-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="3310e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3310e-129">Requirements</span></span>



| <span data-ttu-id="3310e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3310e-130">Requirement</span></span> | <span data-ttu-id="3310e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="3310e-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3310e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3310e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3310e-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3310e-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="3310e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3310e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3310e-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3310e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3310e-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3310e-136">End of server support</span></span><br/>    | <span data-ttu-id="3310e-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3310e-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="3310e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="3310e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3310e-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3310e-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3310e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3310e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3310e-141">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="3310e-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="3310e-142">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="3310e-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="3310e-143">**\_réseau IP**</span><span class="sxs-lookup"><span data-stu-id="3310e-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="3310e-144">**adresse IP du \_ \_ tronçon suivant \_**</span><span class="sxs-lookup"><span data-stu-id="3310e-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="3310e-145">**\_données IP spécifiques \_**</span><span class="sxs-lookup"><span data-stu-id="3310e-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





