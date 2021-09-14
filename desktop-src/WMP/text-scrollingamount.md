---
title: TEXT. scrollingAmount
description: L’attribut scrollingAmount spécifie ou récupère le nombre de pixels que le texte déplace au cours de chaque mouvement de défilement.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- TEXT. scrollingAmount Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66de7bfc6001f10c429d05c480dc315edfe72f76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095586"
---
# <a name="textscrollingamount"></a>TEXT. scrollingAmount

L’attribut **scrollingAmount** spécifie ou récupère le nombre de pixels que le texte déplace au cours de chaque mouvement de défilement.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture positif (**int**) avec une valeur par défaut de 6.

## <a name="remarks"></a>Notes

Pour le défilement Smooth, **scrollingAmount** doit être petit. Pour un dessin rapide avec de grands écarts, le **scrollingAmount** doit être plus grand. Si le **défilement** = « false », **scrollingAmount** est ignoré.

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

 

 





