---
title: EFFECTs. currentEffectType
description: L’attribut currentEffectType spécifie ou récupère le nom du registre de la visualisation actuelle. Ce nom est un ID unique défini par l’auteur de la visualisation.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535898"
---
# <a name="effectscurrenteffecttype"></a>EFFECTs. currentEffectType

L’attribut **currentEffectType** spécifie ou récupère le nom du registre de la visualisation actuelle. Ce nom est un ID unique défini par l’auteur de la visualisation.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Vous pouvez utiliser cet attribut au moment de l’exécution pour modifier l’effet actuellement affiché. Pour ce faire, procédez comme suit :

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

 

 





