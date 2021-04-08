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
# <a name="filtering-sublayer-identifiers"></a>Filtrage des identificateurs de sous-couche

Les identificateurs de sous-couche WFP (Windows Filtering Platform) sont tous représentés par un GUID.

Ces identificateurs sont définis comme suit.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM sous \_ \_ -couche \_ traversée latérale/FWPM \_ \_ TEREDO**
</dt> <dd> <dl> <dt>



Les filtres de parcours Edge sont ajoutés à cette sous-couche.

> [!Note]  
> Pour Windows 7 et versions ultérieures, utilisez la **\_ \_ \_ traversée latérale** de la sous-couche FWPM.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**INSPECTION de la sous- \_ couche FWPM \_**
</dt> <dd> <dl> <dt>



Il s’agit de la sous-couche la moins pondérée. Elle est utilisée uniquement pour les filtres d’inspection.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM sous- \_ couche \_ IPSec \_ DOSP**
</dt> <dd> <dl> <dt>



Les filtres de protection DoS IPsec sont ajoutés à cette sous-couche.

> [!Note]  
> Disponible uniquement sur Windows Vista avec SP1, Windows Server 2008 et versions ultérieures.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_ \_ \_ tunnel sortant de transfert IPSec \_ de sous-couche FWPM \_**
</dt> <dd> <dl> <dt>



Les filtres de tunnel sortant IPsec sont ajoutés à cette sous-couche.

> [!Note]  
> Disponible uniquement sur Windows 7, Windows Server 2008 R2 et versions ultérieures.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_ \_ tunnel IPSec sous-couche FWPM \_**
</dt> <dd> <dl> <dt>



Les filtres de tunnel IPsec sont ajoutés à cette sous-couche.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM sous- \_ couches \_ Lip**
</dt> <dd> <dl> <dt>



Les filtres IPsec hérités sont ajoutés à cette sous-couche.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_ \_ audit RPC de la sous-couche FWPM \_**
</dt> <dd> <dl> <dt>



Les filtres d’audit RPC sont ajoutés à cette sous-couche. Ces filtres auditent les appels entrants RPC dans le cadre de la conformité C2 et des critères communs.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_ \_ Socket sécurisé de sous-couche FWPM \_**
</dt> <dd> <dl> <dt>



Les filtres de socket sécurisés sont ajoutés à cette sous-couche.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ déchargement TCP \_ Chimney \_ de sous-couche FWPM**
</dt> <dd> <dl> <dt>



Les filtres de déchargement TCP Chimney sont ajoutés à cette sous-couche.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_ \_ modèles TCP de sous-couche FWPM \_** 
</dt> <dd> <dl> <dt>



Les filtres de modèle TCP sont ajoutés à cette sous-couche.

> [!Note]  
> Disponible uniquement sur Windows 8, Windows Server 2012 et versions ultérieures.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**sous- \_ couche FWPM \_ universelle**
</dt> <dd> <dl> <dt>



Cette sous-couche héberge tous les filtres qui ne sont affectés à aucune des autres sous-couches.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





