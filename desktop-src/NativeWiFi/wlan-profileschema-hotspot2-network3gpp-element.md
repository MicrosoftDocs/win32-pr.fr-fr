---
description: Liste des ID PLMN (public Land Mobile Network).
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Élément Network3GPP (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cc3cf7663f0e293db5900453141f5869b6ff8e7c8f047f504311423b08e2a6eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984159"
---
# <a name="network3gpp-hotspot2-element"></a>Élément Network3GPP (Hotspot2)

Liste des ID PLMN (public Land Mobile Network).

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
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



| Élément | Type | Description                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| PLMNID  |      | ID PLMN individuel. Il s’agit d’un nombre décimal à 5 ou 6 chiffres correspondant au MCC/MNC d’un réseau 3GPP.<br/> |



 

 




