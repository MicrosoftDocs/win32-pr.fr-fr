---
description: Liste d’identificateurs de domaine NAI (Network Access identifier).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Élément NAIRealm (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527790"
---
# <a name="nairealm-hotspot2-element"></a>Élément NAIRealm (Hotspot2)

Liste d’identificateurs de domaine NAI (Network Access identifier). Les entrées de cette liste sont généralement de la forme `user@domain` . La liste de domaines NAI est la méthode recommandée pour identifier la plupart des opérateurs non mobiles tels que MSO, les opérateurs câblés et les lieux publics.

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
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



| Élément | Type | Description                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Identificateur de domaine unique. Généralement du formulaire `user@domain` . |



 

 



