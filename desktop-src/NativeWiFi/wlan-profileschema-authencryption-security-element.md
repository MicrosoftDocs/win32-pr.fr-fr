---
description: Spécifie l’authentification et la paire de chiffrement à utiliser pour ce profil.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Élément authEncryption (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194811"
---
# <a name="authencryption-security-element"></a>Élément authEncryption (Security)

L’élément authEncryption (Security) spécifie la paire d’authentification et de chiffrement à utiliser pour ce profil.

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="encryption">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="none"
                         />
                        <xs:enumeration
                            value="WEP"
                         />
                        <xs:enumeration
                            value="TKIP"
                         />
                        <xs:enumeration
                            value="AES"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
             />
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

L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type                                                              | Description                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**identification**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Spécifie la méthode d’authentification qui doit être utilisée pour se connecter au réseau local sans fil.<br/> |
| [**chiffre**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Définit le chiffrement des données à utiliser pour se connecter au réseau local sans fil.<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indique si 802.1 X est utilisé.<br/>                                                     |



## <a name="remarks"></a>Notes

L’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) peut être inséré en tant qu’enfant de l’élément **authEncryption** .

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **authEncryption** , consultez Exemples de profils [sans fil](wireless-profile-samples.md). Pour afficher un exemple de profil qui utilise l’élément [**FipsMode**](wlan-profileschema-fipsmode-authencryption-element.md) , consultez [exemple de profil FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de profils sans fil](wireless-profile-samples.md)
</dt> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**caution**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**sécurité (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
