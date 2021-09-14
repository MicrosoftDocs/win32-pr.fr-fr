---
description: Contient le SSID d’un réseau local sans fil.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: nom (SSID), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110389"
---
# <a name="name-ssid-element"></a>nom (SSID), élément

L’élément nom (SSID) contient le SSID d’un réseau local sans fil.

``` syntax
<xs:element name="name">
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
```

L’élément est défini par l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

## <a name="remarks"></a>Notes

Les noms respectent la casse.

Bien que les éléments [**Hex**](wlan-profileschema-hex-ssid-element.md) et **Name** soient facultatifs, au moins un élément **Hex** ou **Name** doit apparaître en tant qu’enfant de l’élément [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

Lorsque les informations de profil sont converties en SSID, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est converti en SSID (le cas échéant) et l’élément **Name** est ignoré. Si l’élément **Hex** n’est pas présent, l’élément **Name** est converti en SSID à l’aide d’une conversion Unicode en ASCII.

Lorsqu’un SSID est stocké dans un profil, l’élément [**Hex**](wlan-profileschema-hex-ssid-element.md) est toujours généré. L’élément **Name** est généré uniquement si la conversion ASCII en Unicode du SSID et de la génération de profil XML réussit. Certaines informations du SSID d’origine peuvent être perdues lorsqu’elles sont converties en un **nom**.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Les caractères d’échappement XML, tels que les &, ne sont pas affichés. évitez d’utiliser des caractères d’échappement XML dans des noms SSID pour les profils déployés sur Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2.

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **Name** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

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

 

 




