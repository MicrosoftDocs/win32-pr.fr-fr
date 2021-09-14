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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919540"
---
# <a name="level-levellisttype-element"></a>Élément Level (LevelListType)

Définit une valeur de gravité qui détermine le niveau de détail des événements lors de la journalisation.

``` syntax
<xs:element name="level"
    type="LevelType"
 />
```

L’élément **Level** est défini par le type complexe [**LevelListType**](eventmanifestschema-levellisttype-complextype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Éléments parents**
</dt> <dt>

[**niveaux (ProviderType)**](eventmanifestschema-levels-providertype-element.md)
</dt> <dt>

[**niveaux (type de données)**](eventmanifestschema-levels-metadatatype-element.md)
</dt> </dl>

 

 





