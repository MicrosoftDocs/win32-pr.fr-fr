---
title: Élément Connection (Connections)
description: Définit chaque paramètre de configuration et l’associe à un nom. L’élément Connection est facultatif.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Élément de connexion EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522713"
---
# <a name="connection-connections-element"></a>Élément Connection (Connections)

L’élément **Connection (Connections)** définit chaque paramètre de configuration et l’associe à un nom. L’élément **Connection** est facultatif.

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **Connection** est défini par l’élément [**connections**](eapconnectionpropertiesv1schema-connections-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                 | Type   | Description                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | Identifie l’élément de configuration EAP.<br/>                                                                    |
| [**Nomme**](eapconnectionpropertiesv1schema-name-connection-element.md) | string | Capture le nom de la connexion définie, en aidant à identifier plusieurs connexions. <br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**Connexions**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Connexions**](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





