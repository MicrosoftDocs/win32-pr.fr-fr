---
description: Spécifie la liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Élément de blocage (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c5bd795ee9f5fc21dc205c24306820b4dec7f074638aa0e4f11ba3acde68cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684419"
---
# <a name="blocklist-networkfilter-element"></a>Élément de blocage (networkFilter)

L’élément de liste de blocage (networkFilter) spécifie la liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.

``` syntax
<xs:element name="blockList">
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

L' **élément de la** en-dessus est défini par l’élément [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                        | Type                                                                     | Description                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [**réseaux**](wlan-policyschema-network-blocklist-element.md) | [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) | Réseau bloqué. <br/> |



## <a name="requirements"></a>Configuration requise



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

 

 




