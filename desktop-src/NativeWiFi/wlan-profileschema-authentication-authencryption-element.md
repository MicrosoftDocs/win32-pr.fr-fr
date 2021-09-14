---
description: Spécifie la méthode d’authentification à utiliser pour se connecter au réseau local sans fil.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Élément Authentication (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194807"
---
# <a name="authentication-authencryption-element"></a>Élément Authentication (authEncryption)

L’élément Authentication (authEncryption) spécifie la méthode d’authentification à utiliser pour se connecter au réseau local sans fil.

``` syntax
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
```

L’élément est défini par l’élément [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Notes

Le tableau suivant décrit les valeurs d’énumération.



| Valeur   | Description                            |
|---------|----------------------------------------|
| ouvert    | Ouvrez l’authentification 802,11.            |
| partagés  | Authentification 802,11 partagée.          |
| WPA     | WPA-Enterprise l’authentification 802,11.  |
| WPAPSK  | WPA-Personal l’authentification 802,11.    |
| WPA2    | WPA2-Enterprise l’authentification 802,11. |
| WPA2PSK | WPA2-Personal l’authentification 802,11.   |



 

Pour plus d’informations sur les méthodes d’authentification 802,11, consultez les spécifications [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)et [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **Authentication** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

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

 

 




