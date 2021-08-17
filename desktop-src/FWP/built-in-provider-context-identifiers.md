---
title: Identificateurs de contexte fournisseur intégrés (Fwpmu. h)
description: Les contextes de fournisseur intégrés identifient les stratégies par défaut à utiliser avec les sockets sécurisés.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0247b58b38de55eb67479c68e0c0955fb9d2a56a793215330366ca8ccfbe4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951328"
---
# <a name="built-in-provider-context-identifiers"></a>Identificateurs de contexte fournisseur intégrés

les identificateurs des contextes de fournisseur intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID. Ces contextes de fournisseur intégrés identifient les stratégies par défaut à utiliser avec les sockets sécurisés.

Ces identificateurs sont définis comme suit.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**contexte du fournisseur FWPM de \_ \_ \_ \_ Socket sécurisé \_ AUTHIP**
</dt> <dd> <dl> <dt>



Stratégie par défaut en mode principal protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP) pour les sockets sécurisés.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_contexte du fournisseur FWPM \_ \_ \_ IPSec Socket sécurisé \_**
</dt> <dd> <dl> <dt>



Stratégie par défaut du mode rapide IPsec (Internet Protocol Security) pour les sockets sécurisés.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





