---
description: Spécifie la liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Élément allowList (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413710"
---
# <a name="allowlist-networkfilter-element"></a>Élément allowList (networkFilter)

L’élément allowList (networkFilter) spécifie la liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter.

``` syntax
<xs:element name="allowList">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="network"
                type="networkItemType"
                maxOccurs="unbounded"
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

L’élément **allowList** est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                        | Type                                                                     | Description                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [**réseaux**](wlan-policyschema-network-allowlist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Réseau auquel la machine peut se connecter.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**networkFilter (WLANPolicy)**](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




