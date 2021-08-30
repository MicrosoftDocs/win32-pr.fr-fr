---
title: AmbientAttributes. Width
description: L’attribut width spécifie ou récupère la largeur du contrôle.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- AmbientAttributes. width Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc78b23dbedf75b7a58a16fc4aaa43413272c22e6513acbd13b5a6cd890e3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004099"
---
# <a name="ambientattributeswidth"></a>AmbientAttributes. Width

L’attribut **Width** spécifie ou récupère la largeur du contrôle.

``` syntax
        elementID.width
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **entier** 16 bits en lecture/écriture (0 à 32 767) représentant la largeur du contrôle en pixels. La valeur par défaut est zéro ou la largeur de l’image spécifiée dans l’attribut **image** du contrôle.

## <a name="remarks"></a>Remarques

Si la largeur spécifiée est plus étroite que la largeur de l’image fournie, l’image est découpée. Si la largeur est plus large que la largeur de l’image, la zone de clic va au-delà de la limite de l’image. Quelle que soit la valeur attribuée à cet attribut, l’image ne peut pas croître au-delà de la **vue** ou de la sous- **vue** parente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





