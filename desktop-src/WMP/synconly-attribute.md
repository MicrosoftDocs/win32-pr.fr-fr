---
title: Attribut SyncOnly
description: L’attribut SyncOnly est une représentation sous forme de chaîne d’une valeur booléenne utilisée par le lecteur Windows Media pour déterminer si une sélection est disponible uniquement pour la synchronisation.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Attribut SyncOnly lecteur Windows Media
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541026"
---
# <a name="synconly-attribute"></a>Attribut SyncOnly

L’attribut **SyncOnly** est une représentation sous forme de chaîne d’une valeur **booléenne** utilisée par le lecteur Windows Media pour déterminer si une sélection est disponible uniquement pour la synchronisation.

## <a name="applies-to"></a>S'applique à

-   [Sélections](playlist-attributes-ref.md)

## <a name="remarks"></a>Notes

La valeur 1 indique que la sélection est disponible uniquement pour la synchronisation et ne peut pas apparaître dans le nœud **sélection automatique** . La valeur zéro indique que la sélection peut apparaître dans le nœud **sélection automatique** .

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





