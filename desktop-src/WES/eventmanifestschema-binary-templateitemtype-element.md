---
title: Élément Binary (TemplateItemType)
description: Contient les données binaires fournies par l’API du journal des événements.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- élément binaire EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517320"
---
# <a name="binary-templateitemtype-element"></a>Élément Binary (TemplateItemType)

Contient les données binaires fournies par l’API du [Journal des événements](/windows/desktop/EventLog/event-logging) .

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément **binaire** est défini par le type complexe [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom | Type   | Description                                          |
|------|--------|------------------------------------------------------|
| name | string | Nom associé aux données binaires.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**modèle (TemplateListType)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

