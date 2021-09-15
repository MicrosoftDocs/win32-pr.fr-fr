---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Définition du ODJ_POLICY_DNS_DOMAIN_INFO IDL
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517793"
---
# <a name="odj_policy_dns_domain_info-structure"></a>Structure ODJ_POLICY_DNS_DOMAIN_INFO

Contient des informations sur le domaine et la forêt auxquels un client doit être joint.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a>Membres

### <a name="name"></a>Nom

Doit être défini sur un nom de domaine NetBIOS.

### <a name="dnsdomainname"></a>DnsDomainName

Doit être défini sur un nom de domaine au format DNS.

### <a name="dnsforestname"></a>DnsForestName

Doit être défini sur un nom de forêt au format DNS.

### <a name="domainguid"></a>DomainGuid

Doit être défini sur le GUID du domaine.

### <a name="sid"></a>SID

Doit être défini sur le SID du domaine.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**\_chaîne Unicode \_ ODJ**](odj-odj_unicode_string.md)

[**\_sid ODJ**](odj-odj_sid.md)
