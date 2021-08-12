---
title: Élément clockType (ChannelPublishingType)
description: Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement.
ms.assetid: dc2ed9d0-782c-44c9-aa55-ca6ff340f413
keywords:
- EventLog, élément clockType
topic_type:
- apiref
api_name:
- clockType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fde3b263c2a190e91fdd2ddde8f05a40e9026486195ca9ae95b5f98cdcf7733d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590030"
---
# <a name="clocktype-channelpublishingtype-element"></a>Élément clockType (ChannelPublishingType)

Résolution d’horloge à utiliser lors de la journalisation de l’horodatage pour chaque événement.

``` syntax
<xs:element name="clockType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="SystemTime"
             />
            <xs:enumeration
                value="QPC"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **clockType** est défini par le type complexe [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**publication (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





