---
title: TEXT. scrollingDelay
description: L’attribut scrollingDelay spécifie ou récupère le délai entre les mouvements de défilement.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- TEXT. scrollingDelay Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095585"
---
# <a name="textscrollingdelay"></a>TEXT. scrollingDelay

L’attribut **scrollingDelay** spécifie ou récupère le délai entre les mouvements de défilement.

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**int**) qui spécifie le délai en millisecondes. Elle a une valeur minimale de 30 et une valeur par défaut de 85. Si une valeur inférieure à la valeur minimale est spécifiée, la valeur par défaut est utilisée.

## <a name="remarks"></a>Notes

Si le **défilement** est défini sur false, **scrollingDelay** est ignoré.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXTE. défilement**](text-scrolling.md)
</dt> </dl>

 

 





