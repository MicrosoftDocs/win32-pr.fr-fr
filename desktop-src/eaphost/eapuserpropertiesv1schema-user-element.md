---
title: Élément User
description: En savoir plus sur l’élément utilisateur. Cet élément n’est pas utilisé lors de l’utilisation de méthodes héritées via les API EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Élément utilisateur EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730364"
---
# <a name="user-element"></a>Élément User

L’élément **User** n’est pas utilisé lors de l’utilisation de méthodes héritées via les API EAPHost.

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                  | Type | Description                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) |      | Capture les informations d’identification spécifiques au type de méthode et à la méthode.<br/> |



## <a name="requirements"></a>Configuration requise



| Role | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





