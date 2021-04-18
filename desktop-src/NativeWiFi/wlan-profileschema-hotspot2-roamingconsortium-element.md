---
description: Liste des identificateurs uniques (OUI) attribués par IEEE.
ms.assetid: 4a9885b6-2e57-4a16-8e1d-b5b0797e09db
title: Élément RoamingConsortium (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RoamingConsortium
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5e53fa274cbc56de6be026ef0e466ec501cf9124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519575"
---
# <a name="roamingconsortium-hotspot2-element"></a>Élément RoamingConsortium (Hotspot2)

Liste des identificateurs uniques (OUI) attribués par IEEE.

``` syntax
<xs:element name="RoamingConsortium"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="3"
                         />
                        <xs:maxLength
                            value="5"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément est défini par l’élément [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément | Type | Description                                                               |
|---------|------|---------------------------------------------------------------------------|
| OUI     |      | OUI unique, mise en forme en tant que nombre hexadécimal de taille variable.<br/> |



 

 




