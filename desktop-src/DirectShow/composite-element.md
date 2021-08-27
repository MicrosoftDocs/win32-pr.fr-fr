---
description: L’élément composite définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Élément composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec9ce7c889829ee227ce31df25d5d17985e877ed107870170f6939aebf14fd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084309"
---
# <a name="composite-element"></a>Élément composite

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `composite` élément définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.

## <a name="attributes"></a>Attributs

[**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **groupe**](group-element.md)                                                                             |
| Children | `composite`, [**Effect**](effect-element.md), [**Track**](track-element.md), [**transition**](transition-element.md) |



 

## <a name="remarks"></a>Remarques

Dans un `composite` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément. La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.

## <a name="examples"></a>Exemples


```XML
<composite> </composite>
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



