---
description: Contient un SSID pour un réseau local sans fil.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Élément SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866030"
---
# <a name="ssid-ssidconfig-element"></a>Élément SSID (SSIDConfig)

L’élément SSID (SSIDConfig) contient un SSID pour un réseau local sans fil.

**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Au plus un élément **SSID** peut apparaître dans un profil.

``` syntax
<xs:element name="SSID"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="hex"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="32"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="name"
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
                            value="32"
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

L’élément **SSID** est défini par l’élément [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                              | Type | Description                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Contient le SSID d’un réseau local sans fil au format hexadécimal.<br/> |
| [**nomme**](wlan-profileschema-name-ssid-element.md) |      | Contient le SSID d’un réseau local sans fil.<br/>                      |



## <a name="remarks"></a>Notes

Bien que les éléments [**Hex**](wlan-profileschema-hex-ssid-element.md) et [**Name**](wlan-profileschema-name-ssid-element.md) soient facultatifs, au moins un élément **Hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) doit apparaître en tant qu’enfant de l’élément **SSID** .

Lorsque les informations de profil sont converties en SSID, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est converti en SSID (le cas échéant) et l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est ignoré. Si l’élément **Hex** n’est pas présent, l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est converti en SSID à l’aide d’une conversion Unicode en ASCII.

Lorsqu’un SSID est stocké dans un profil, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est toujours généré. L’élément [**Name**](wlan-profileschema-name-ssid-element.md) est généré uniquement si la conversion ASCII en Unicode du SSID et de la génération de profil XML réussit. Certaines informations du SSID d’origine peuvent être perdues lorsqu’elles sont converties en un [**nom**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **SSID** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




