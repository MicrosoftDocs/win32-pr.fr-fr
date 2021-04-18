---
title: Élément Level (LevelListType)
description: Définit une valeur de gravité qui détermine le niveau de détail des événements lors de la journalisation.
ms.assetid: 898b4784-7acc-45b5-8ff9-485e919fe9c6
keywords:
- élément de niveau EventLog
topic_type:
- apiref
api_name:
- level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 469ed05f6acb7b4189afdadda772982441fdb435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536296"
---
# <a name="level-levellisttype-element"></a>Élément Level (LevelListType)

Définit une valeur de gravité qui détermine le niveau de détail des événements lors de la journalisation.

``` syntax
<xs:element name="level"
    type="LevelType"
 />
```

L’élément **Level** est défini par le type complexe [**LevelListType**](eventmanifestschema-levellisttype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Éléments parents**
</dt> <dt>

[**niveaux (ProviderType)**](eventmanifestschema-levels-providertype-element.md)
</dt> <dt>

[**niveaux (type de données)**](eventmanifestschema-levels-metadatatype-element.md)
</dt> </dl>

 

 





