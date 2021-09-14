---
description: Contient le SSID d’un réseau local sans fil au format hexadécimal.
ms.assetid: 6c49a3e6-f167-408b-a96f-5b6032108f34
title: Élément hex (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- hex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6bc214f50788fdc6965a1ce429c5c2919846cf72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194768"
---
# <a name="hex-ssid-element"></a>Élément hex (SSID)

L’élément hex (SSID) contient le SSID d’un réseau local sans fil au format hexadécimal.

``` syntax
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
```

L’élément est défini par l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Notes

Bien que les éléments **Hex** et [**Name**](wlan-profileschema-name-ssid-element.md) soient facultatifs, au moins un élément **Hex** ou [**Name**](wlan-profileschema-name-ssid-element.md) doit apparaître en tant qu’enfant de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Lorsque les informations de profil sont converties en SSID, l’élément **Hex** est converti en SSID (le cas échéant) et l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est ignoré. Si l’élément **Hex** n’est pas présent, l’élément [**Name**](wlan-profileschema-name-ssid-element.md) est converti en SSID à l’aide d’une conversion Unicode en ASCII.

Lorsqu’un SSID est stocké dans un profil, l’élément **Hex** est toujours généré. L’élément [**Name**](wlan-profileschema-name-ssid-element.md) est généré uniquement si la conversion ASCII en Unicode du SSID et de la génération de profil XML réussit. Certaines informations du SSID d’origine peuvent être perdues lorsqu’elles sont converties en un [**nom**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Exemples

Pour afficher un exemple de profil qui utilise l’élément **Hex** , consultez [exemple de profil FIPS](fips-profile-sample.md).

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

[**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




