---
description: L’élément at définit la valeur d’un élément param à un moment donné, par rapport au début de la transition ou de l’effet qui contient le paramètre.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Élément at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d67a5e3c3ca2bd47381084ad0e0090d7aa208db87f35e5efe3a7d805a73d097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824389"
---
# <a name="at-element"></a>Élément at

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `at` élément définit la valeur d’un élément [**param**](param-element.md) à un moment donné, par rapport au début de la transition ou de l’effet qui contient le paramètre. L' `at` élément amène le paramètre à passer brusquement à la nouvelle valeur à l’heure spécifiée. Pour une progression fluide vers une nouvelle valeur, utilisez l’élément [**linéaire**](linear-element.md) .

## <a name="attributes"></a>Attributs

[**heure**](time-attribute.md), [ **valeur**](value-attribute.md)

## <a name="parentchild-information"></a>Informations parent/enfant



| Étiquette | Valeur |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | Aucun                           |



 

## <a name="examples"></a>Exemples


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments XTL](xtl-elements.md)
</dt> </dl>

 

 



