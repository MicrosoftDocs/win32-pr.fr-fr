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
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464234"
---
# <a name="built-in-provider-context-identifiers"></a>Identificateurs de contexte fournisseur intégrés

Les identificateurs des contextes de fournisseur intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID. Ces contextes de fournisseur intégrés identifient les stratégies par défaut à utiliser avec les sockets sécurisés.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





