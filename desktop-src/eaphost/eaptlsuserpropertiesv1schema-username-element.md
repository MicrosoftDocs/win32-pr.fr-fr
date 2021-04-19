---
title: Élément username (TLS)
description: En savoir plus sur l’élément username. Cet élément capture le nom d’utilisateur à envoyer dans la réponse EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Élément username EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106511513"
---
# <a name="username-element-tls"></a>Élément username (TLS)

L’élément **username** capture le nom d’utilisateur à envoyer dans la réponse EAP-Identity.

Si l’élément **username** est absent, EAP-TLS utilise le nom figurant dans le certificat auquel il est fait appel dans l’élément [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Configuration requise



| Role | Versions de système d’exploitation minimales prises en charge |
|------|-------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





