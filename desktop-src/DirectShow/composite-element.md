---
description: L’élément composite définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Élément composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517149"
---
# <a name="composite-element"></a>Élément composite

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `composite` élément définit une composition, un objet conteneur pour les pistes et d’autres compositions imbriquées.

## <a name="attributes"></a>Attributs

[**Lock**](lock-attribute.md), [**muet**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **groupe**](group-element.md)                                                                             |
| Children | `composite`, [**Effect**](effect-element.md), [**Track**](track-element.md), [**transition**](transition-element.md) |



 

## <a name="remarks"></a>Notes

Dans un `composite` élément, la priorité des couches imbriquées est déterminée implicitement par l’ordre dans lequel elles apparaissent dans l’élément. La première couche a la priorité 0 et les couches suivantes comportent des valeurs de priorité accrues.

## <a name="examples"></a>Exemples


```XML
<composite> </composite>
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



