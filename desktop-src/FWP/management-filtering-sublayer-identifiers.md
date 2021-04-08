---
title: Filtrage des identificateurs de sous-couche (Fwpmu. h)
description: Constantes d’identificateur de sous-couche de filtrage de la gestion des API WFP.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844073"
---
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="5159b-103">Filtrage des identificateurs de sous-couche</span><span class="sxs-lookup"><span data-stu-id="5159b-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="5159b-104">Les identificateurs de sous-couche WFP (Windows Filtering Platform) sont tous représentés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="5159b-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="5159b-105">Ces identificateurs sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="5159b-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="5159b-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM sous \_ \_ -couche \_ traversée latérale/FWPM \_ \_ TEREDO**</span><span class="sxs-lookup"><span data-stu-id="5159b-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-107">Les filtres de parcours Edge sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5159b-108">Pour Windows 7 et versions ultérieures, utilisez la **\_ \_ \_ traversée latérale** de la sous-couche FWPM.</span><span class="sxs-lookup"><span data-stu-id="5159b-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**INSPECTION de la sous- \_ couche FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5159b-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-110">Il s’agit de la sous-couche la moins pondérée.</span><span class="sxs-lookup"><span data-stu-id="5159b-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="5159b-111">Elle est utilisée uniquement pour les filtres d’inspection.</span><span class="sxs-lookup"><span data-stu-id="5159b-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM sous- \_ couche \_ IPSec \_ DOSP**</span><span class="sxs-lookup"><span data-stu-id="5159b-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-113">Les filtres de protection DoS IPsec sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5159b-114">Disponible uniquement sur Windows Vista avec SP1, Windows Server 2008 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5159b-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_ \_ \_ tunnel sortant de transfert IPSec \_ de sous-couche FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5159b-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-116">Les filtres de tunnel sortant IPsec sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5159b-117">Disponible uniquement sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5159b-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_ \_ tunnel IPSec sous-couche FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5159b-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-119">Les filtres de tunnel IPsec sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM sous- \_ couches \_ Lip**</span><span class="sxs-lookup"><span data-stu-id="5159b-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-121">Les filtres IPsec hérités sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_ \_ audit RPC de la sous-couche FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5159b-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-123">Les filtres d’audit RPC sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="5159b-124">Ces filtres auditent les appels entrants RPC dans le cadre de la conformité C2 et des critères communs.</span><span class="sxs-lookup"><span data-stu-id="5159b-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_ \_ Socket sécurisé de sous-couche FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5159b-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-126">Les filtres de socket sécurisés sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ déchargement TCP \_ Chimney \_ de sous-couche FWPM**</span><span class="sxs-lookup"><span data-stu-id="5159b-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-128">Les filtres de déchargement TCP Chimney sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_ \_ modèles TCP de sous-couche FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5159b-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-130">Les filtres de modèle TCP sont ajoutés à cette sous-couche.</span><span class="sxs-lookup"><span data-stu-id="5159b-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5159b-131">Disponible uniquement sur Windows 8, Windows Server 2012 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5159b-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5159b-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**sous- \_ couche FWPM \_ universelle**</span><span class="sxs-lookup"><span data-stu-id="5159b-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5159b-133">Cette sous-couche héberge tous les filtres qui ne sont affectés à aucune des autres sous-couches.</span><span class="sxs-lookup"><span data-stu-id="5159b-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5159b-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5159b-134">Requirements</span></span>



| <span data-ttu-id="5159b-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5159b-135">Requirement</span></span> | <span data-ttu-id="5159b-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5159b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5159b-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5159b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5159b-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5159b-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5159b-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5159b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5159b-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5159b-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5159b-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="5159b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5159b-142"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5159b-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





