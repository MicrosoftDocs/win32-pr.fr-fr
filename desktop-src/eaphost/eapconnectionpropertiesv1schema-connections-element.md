---
title: Élément connections
description: En savoir plus sur l’élément Connections. Cet élément collecte et contient zéro ou plusieurs éléments de connexion.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Connections, élément EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62635d09030875a4f17deefa1aec05432df5662369eb483894f1a8cef4bbaf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498217"
---
# <a name="connections-element"></a>Élément connections

L’élément **connections** collecte et contient zéro ou plusieurs éléments de [**connexion**](eapconnectionpropertiesv1schema-connection-connections-element.md) .

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                              | Type   | Description                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | Identifie l’élément de configuration EAP.<br/>                                                                                                                                       |
| [**Connexion**](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | Définit chaque paramètre de configuration et l’associe à un nom. L’élément [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) est facultatif.<br/> |
| [**Nom**](eapconnectionpropertiesv1schema-name-connection-element.md)              | string | Capture le nom de la connexion définie, en aidant à identifier plusieurs connexions.<br/>                                                                     |



## <a name="remarks"></a>Remarques

L’élément **connections** n’est pas utilisé avec les méthodes héritées via les API EAPHost.

## <a name="requirements"></a>Configuration requise



| Fonction | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





