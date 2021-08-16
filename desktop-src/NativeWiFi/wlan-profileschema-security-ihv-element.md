---
description: Contient différents paramètres de sécurité utilisés par des fournisseurs de matériel indépendants.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Élément Security (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e4baeadc5e53dc53d0a526b62c4905da1a778a1015f58321ae8b96e4aa52dfcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912749"
---
# <a name="security-ihv-element"></a>Élément Security (IHV)

L’élément Security (IHV) contient différents paramètres de sécurité utilisés par des fournisseurs de matériel indépendants.

Les paramètres de sécurité Microsoft et les paramètres de sécurité IHV s’excluent mutuellement. Si les deux jeux de paramètres de sécurité sont présents dans le même profil, le profil n’est pas valide.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **Security** est défini par l’élément [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .

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

 

 




