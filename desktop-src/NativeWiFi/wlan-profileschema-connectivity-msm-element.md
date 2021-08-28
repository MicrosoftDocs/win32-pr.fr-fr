---
description: Contient différents paramètres de connectivité.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: Élément de connectivité (MSM)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8745671004799f96aecfe68b531c122c76122b5865678258fd241e9d8a07260a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799909"
---
# <a name="connectivity-msm-element"></a>Élément de connectivité (MSM)

L’élément de connectivité (MSM) contient différents paramètres de connectivité.

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
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

L’élément est défini par l’élément [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                            | Type |
|--------------------------------------------------------------------|------|
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément de **connectivité** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MSM**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




