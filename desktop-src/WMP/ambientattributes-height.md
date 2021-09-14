---
title: AmbientAttributes. Height
description: L’attribut Height spécifie ou récupère la hauteur du contrôle.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes. height Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856173"
---
# <a name="ambientattributesheight"></a>AmbientAttributes. Height

L’attribut **Height** spécifie ou récupère la hauteur du contrôle.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) représentant la hauteur du contrôle en pixels. La valeur par défaut est zéro ou la hauteur de l’image spécifiée dans l’attribut **image** du contrôle.

## <a name="remarks"></a>Notes

Si la hauteur spécifiée est inférieure à la hauteur de l’image fournie, l’image est découpée. Si la hauteur est supérieure à la hauteur de l’image, la zone de clic va au-delà de la limite de l’image. Quelle que soit la valeur attribuée à cet attribut, l’image ne peut pas croître au-delà de la **vue** ou de la sous- **vue** parente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





