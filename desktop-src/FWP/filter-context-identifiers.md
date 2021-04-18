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
# <a name="filter-context-identifiers"></a>Identificateurs de contexte de filtre

Les identificateurs des contextes de filtre intégrés à la plateforme de filtrage Windows sont définis comme suit.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**\_ \_ relais entrant IPSec FWPM Context \_ \_ , FWPM \_ contexte \_ IPSec \_ entrant \_ persister \_ \_ , sécurité de connexion \_ \_ \_ \_ non liée IPSec de contexte FWPM**
</dt> <dd> <dl> <dt>



Contextes de filtre de transport IPsec dans la couche entrante.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**\_ \_ \_ découverte négociation IPSec sortante FWPM Context IPSec \_ \_ , \_ \_ négociation des \_ suppressions sortantes IPSec \_ de contexte FWPM \_**
</dt> <dd> <dl> <dt>



Contextes de filtre de transport IPsec dans une couche sortante.

> [!Note]  
> Pour Windows 7, utilisez **la \_ négociation de suppression du contexte \_ IPSec \_ sortants \_ \_ FWPM**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM \_ Context \_ ALE \_ Set \_ Connection \_ requièrent la \_ \_ sécurité IPSec, FWPM \_ Context \_ ALE \_ Set \_ connexion \_ Lazy \_ SD \_ évaluation**
</dt> <dd> <dl> <dt>



Filtrez les contextes utilisés dans la couche de connexion ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM \_ Context \_ ALE \_ Set \_ Connection \_ nécessite \_ le \_ chiffrement IPSec, FWPM \_ Context \_ ALE \_ Set \_ Connection \_ allow \_ First \_ \_ \_ Encrypted PKT non chiffré, FWPM \_ Context \_ PEA \_ allow \_ auth \_ FW**
</dt> <dd> <dl> <dt>



Filtrez les contextes utilisés dans la couche de connexion ALE ou d’acceptation.

> [!Note]  
> Pour Windows 7, utilisez **FWPM \_ Context \_ ALE \_ Set \_ Connection \_ autoriser \_ First \_ \_ \_ Encrypted PKT non chiffré** ou **FWPM \_ Context \_ PEA \_ allow \_ auth \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_contexte FWPM \_ Activation \_ du \_ déchargement TCP Chimney \_ , \_ \_ \_ \_ désactivation du déchargement TCP Chimney du contexte FWPM \_**
</dt> <dd> <dl> <dt>



Contextes utilisés par les légendes de déchargement TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_audit RPC du contexte FWPM \_ \_ \_ activé**
</dt> <dd> <dl> <dt>



Contextes utilisés dans la sous-couche d’audit RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





