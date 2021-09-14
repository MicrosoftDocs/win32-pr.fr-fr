---
title: Élément sidType (ChannelPublishingType)
description: Détermine s’il faut inclure un identificateur de sécurité (SID) du principal avec chaque événement écrit dans le canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- EventLog, élément sidType
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193336"
---
# <a name="sidtype-channelpublishingtype-element"></a>Élément sidType (ChannelPublishingType)

Détermine s’il faut inclure un identificateur de sécurité (SID) du principal avec chaque événement écrit dans le canal.

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **sidType** est défini par le type complexe [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**publication (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





