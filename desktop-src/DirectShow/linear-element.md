---
description: L’élément Linear définit la valeur d’un élément param à un moment donné, par rapport au début de la transition ou de l’effet qui contient l’élément param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Élément linéaire (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007502"
---
# <a name="linear-element"></a>Élément linéaire

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L’élément Linear définit la valeur d’un élément [**param**](param-element.md) à un moment donné, par rapport au début de la transition ou de l’effet qui contient l’élément **param** . L' `linear` élément fait en sorte que le paramètre effectue une transition en douceur de sa valeur précédente à la nouvelle valeur. Pour obtenir un saut instantané vers une nouvelle valeur, utilisez l’élément [**at**](at-element.md) .

## <a name="attributes"></a>Attributs

[**heure**](time-attribute.md), [ **valeur**](value-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | Aucun                           |



 

## <a name="examples"></a>Exemples


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 




