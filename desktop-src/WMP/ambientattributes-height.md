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
ms.openlocfilehash: 5cbc03f631fffc4d1544906721476f229cbeb926e5d56b08dc1647f2dfd3b243
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098949"
---
# <a name="ambientattributesheight"></a>AmbientAttributes. Height

L’attribut **Height** spécifie ou récupère la hauteur du contrôle.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) représentant la hauteur du contrôle en pixels. La valeur par défaut est zéro ou la hauteur de l’image spécifiée dans l’attribut **image** du contrôle.

## <a name="remarks"></a>Remarques

Si la hauteur spécifiée est inférieure à la hauteur de l’image fournie, l’image est découpée. Si la hauteur est supérieure à la hauteur de l’image, la zone de clic va au-delà de la limite de l’image. Quelle que soit la valeur attribuée à cet attribut, l’image ne peut pas croître au-delà de la **vue** ou de la sous- **vue** parente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





