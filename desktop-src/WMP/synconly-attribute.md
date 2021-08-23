---
title: Attribut SyncOnly
description: l’attribut SyncOnly est une représentation sous forme de chaîne d’une valeur booléenne que Lecteur Windows Media utilise pour déterminer si une sélection est disponible uniquement pour la synchronisation.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Lecteur Windows Media de l’attribut SyncOnly
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77fe67fe3cb943ad210f4d9beb58cfea8f32da87e6ee15955b578f07a608f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134732"
---
# <a name="synconly-attribute"></a>Attribut SyncOnly

l’attribut **SyncOnly** est une représentation sous forme de chaîne d’une valeur **booléenne** que Lecteur Windows Media utilise pour déterminer si une sélection est disponible uniquement pour la synchronisation.

## <a name="applies-to"></a>S'applique à

-   [Sélections](playlist-attributes-ref.md)

## <a name="remarks"></a>Remarques

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

 

 





