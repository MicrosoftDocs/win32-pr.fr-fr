---
title: Identificateurs de contexte de filtre (Fwpmu. h)
description: Identificateurs des contextes de filtre intégrés à la plateforme de filtrage Windows.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512602"
---
# <a name="filter-context-identifiers"></a><span data-ttu-id="dd1e1-103">Identificateurs de contexte de filtre</span><span class="sxs-lookup"><span data-stu-id="dd1e1-103">Filter Context Identifiers</span></span>

<span data-ttu-id="dd1e1-104">Les identificateurs des contextes de filtre intégrés à la plateforme de filtrage Windows sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-104">The identifiers for the filter contexts that are built in to the Windows Filtering Platform are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="dd1e1-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**\_ \_ relais entrant IPSec FWPM Context \_ \_ , FWPM \_ contexte \_ IPSec \_ entrant \_ persister \_ \_ , sécurité de connexion \_ \_ \_ \_ non liée IPSec de contexte FWPM**</span><span class="sxs-lookup"><span data-stu-id="dd1e1-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PASSTHRU, FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY, FWPM\_CONTEXT\_IPSEC\_INBOUND\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dd1e1-106">Contextes de filtre de transport IPsec dans la couche entrante.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-106">IPsec transport filter contexts in inbound layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd1e1-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**\_ \_ \_ découverte négociation IPSec sortante FWPM Context IPSec \_ \_ , \_ \_ négociation des \_ suppressions sortantes IPSec \_ de contexte FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dd1e1-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER, FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dd1e1-108">Contextes de filtre de transport IPsec dans une couche sortante.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-108">IPsec transport filter contexts in outbound layer.</span></span>

> [!Note]  
> <span data-ttu-id="dd1e1-109">Pour Windows 7, utilisez **la \_ négociation de suppression du contexte \_ IPSec \_ sortants \_ \_ FWPM**.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-109">For Windows 7, use **FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd1e1-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ Context \_ ALE \_ Set \_ Connection \_ requièrent la \_ \_ sécurité IPSec, FWPM \_ Context \_ ALE \_ Set \_ connexion \_ Lazy \_ SD \_ évaluation**</span><span class="sxs-lookup"><span data-stu-id="dd1e1-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_SECURITY, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_LAZY\_SD\_EVALUATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dd1e1-111">Filtrez les contextes utilisés dans la couche de connexion ALE.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-111">Filter contexts used in the ALE connect layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd1e1-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ Context \_ ALE \_ Set \_ Connection \_ nécessite \_ le \_ chiffrement IPSec, FWPM \_ Context \_ ALE \_ Set \_ Connection \_ allow \_ First \_ \_ \_ Encrypted PKT non chiffré, FWPM \_ Context \_ PEA \_ allow \_ auth \_ FW**</span><span class="sxs-lookup"><span data-stu-id="dd1e1-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED, FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dd1e1-113">Filtrez les contextes utilisés dans la couche de connexion ALE ou d’acceptation.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-113">Filter contexts used in the ALE connect or accept layer.</span></span>

> [!Note]  
> <span data-ttu-id="dd1e1-114">Pour Windows 7, utilisez **FWPM \_ Context \_ ALE \_ Set \_ Connection \_ autoriser \_ First \_ \_ \_ Encrypted PKT non chiffré** ou **FWPM \_ Context \_ PEA \_ allow \_ auth \_ FW**.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-114">For Windows 7, use **FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED** or **FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd1e1-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_contexte FWPM \_ Activation \_ du \_ déchargement TCP Chimney \_ , \_ \_ \_ \_ désactivation du déchargement TCP Chimney du contexte FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="dd1e1-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_ENABLE, FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_DISABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dd1e1-116">Contextes utilisés par les légendes de déchargement TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-116">Contexts used by the TCP Chimney Offload callouts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd1e1-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_audit RPC du contexte FWPM \_ \_ \_ activé**</span><span class="sxs-lookup"><span data-stu-id="dd1e1-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM\_CONTEXT\_RPC\_AUDIT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dd1e1-118">Contextes utilisés dans la sous-couche d’audit RPC.</span><span class="sxs-lookup"><span data-stu-id="dd1e1-118">Contexts used in the RPC audit sublayer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd1e1-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd1e1-119">Requirements</span></span>



| <span data-ttu-id="dd1e1-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd1e1-120">Requirement</span></span> | <span data-ttu-id="dd1e1-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd1e1-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1e1-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd1e1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1e1-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd1e1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dd1e1-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd1e1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1e1-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd1e1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dd1e1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd1e1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd1e1-127"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1e1-127"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





