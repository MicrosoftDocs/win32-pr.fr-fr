---
description: Identifie le IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Élément OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5293a6e69c1384922572764674cbadd9980702c49f8945518ff9b0c56beee2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797919"
---
# <a name="ouiheader-ihv-element"></a>Élément OUIHeader (IHV)

L’élément OUIHeader (IHV) identifie le IHV.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément est défini par l’élément [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                   | Type | Description                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)   |      | Contient une hexBinary de 3 octets qui identifie le IHV.<br/>                            |
| [**entrer**](wlan-profileschema-type-ouiheader-element.md) |      | Contient une valeur hexBinary de 1 octet qui est utilisée pour différencier les cartes réseau par le même IHV.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**FABRICANTS**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




