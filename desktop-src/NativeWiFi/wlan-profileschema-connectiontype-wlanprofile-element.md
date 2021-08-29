---
description: Indique le mode de fonctionnement du réseau.
ms.assetid: b71de38a-6373-4d96-90dd-a3ad4a7de074
title: Élément connectionType (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 01eec035fdd42504e3c3da0baec537b096d42c63deb7c336d8446bc7a0d95572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799899"
---
# <a name="connectiontype-wlanprofile-element"></a>Élément connectionType (WLANProfile)

L’élément connectionType (WLANProfile) indique le mode de fonctionnement du réseau.

La valeur **ESS** indique un réseau d’infrastructure, tandis que **IBSS** indique un réseau ad hoc.

``` syntax
<xs:element name="connectionType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="IBSS"
             />
            <xs:enumeration
                value="ESS"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **ConnectionType** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **ConnectionType** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




