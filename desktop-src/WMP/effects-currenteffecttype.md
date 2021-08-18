---
title: EFFECTs. currentEffectType
description: L’attribut currentEffectType spécifie ou récupère le nom du registre de la visualisation actuelle. Ce nom est un ID unique défini par l’auteur de la visualisation.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- effects. currentEffectType Lecteur Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df55ae806781fa0924349cfe472f355cdabd2be6723148fc6100dc39efd9062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996749"
---
# <a name="effectscurrenteffecttype"></a>EFFECTs. currentEffectType

L’attribut **currentEffectType** spécifie ou récupère le nom du registre de la visualisation actuelle. Ce nom est un ID unique défini par l’auteur de la visualisation.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cet attribut au moment de l’exécution pour modifier l’effet actuellement affiché. Pour cela, procédez comme suit :

1.  Utilisez **effectCount** pour récupérer le nombre d’effets enregistrés.
2.  Dans une boucle, récupérez le nom de chaque effet enregistré à l’aide de **effectType**.
3.  Spécifiez l’un des noms que vous avez récupérés pour **currentEffectType** pour définir l’effet actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTs. effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTs. effectType**](effects-effecttype.md)
</dt> </dl>

 

 





