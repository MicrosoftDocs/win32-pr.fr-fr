---
description: Indique si la connexion à un réseau local sans fil doit être automatique ou lancée par l’utilisateur.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Élément connectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753756"
---
# <a name="connectionmode-wlanprofile-element"></a>Élément connectionMode (WLANProfile)

L’élément connectionMode (WLANProfile) indique si la connexion à un réseau local sans fil doit être automatique ou lancée par l’utilisateur.

Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur ESS, cette valeur peut être automatique ou manuelle. La valeur par défaut est auto si cet élément est absent.

Si [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) est défini sur IBSS, cette valeur doit être manuelle.

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **connectionMode** est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="remarks"></a>Notes

Le tableau suivant décrit les valeurs d’énumération.



| Valeur  | Description                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| auto   | La connexion au réseau sans fil doit être lancée automatiquement chaque fois que le réseau est à portée. |
| manual | La connexion au réseau sans fil est uniquement initialisée par sur la demande explicite d’un utilisateur.               |



 

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **connectionMode** , consultez Exemples de profils [sans fil](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




