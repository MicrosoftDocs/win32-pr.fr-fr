---
description: Spécifie le type de chiffrement des données à utiliser pour se connecter à un réseau local sans fil.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Élément Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194776"
---
# <a name="encryption-authencryption-element"></a>Élément Encryption (authEncryption)

L’élément Encryption (authEncryption) spécifie le type de chiffrement des données à utiliser pour se connecter à un réseau local sans fil.

``` syntax
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
```

L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Notes

Lorsque l’élément de **chiffrement** a la valeur WEP, [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) doit être défini sur **networkKey**.

La méthode de chiffrement AES est spécifiée dans les spécifications [802.1 x](https://ieeexplore.ieee.org/document/1438730) et [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément de **chiffrement** , consultez [exemples de profils sans fil](wireless-profile-samples.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**authEncryption (sécurité)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




