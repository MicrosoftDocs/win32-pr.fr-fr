---
title: BUTTONGROUP. hoverImage
description: L’attribut hoverImage spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le BUTTONGROUP. L’état de survol se produit lorsque le bouton est à l’État haut et que l’utilisateur pointe dessus avec la souris.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP. hoverImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee872c06d405d0f9cf5c09f59a86ba1962d0a5b349460c978e37fb5022f1d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135902"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP. hoverImage

L’attribut **hoverImage** spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le **BUTTONGROUP**. L’état de survol se produit lorsque le bouton est à l’État haut et que l’utilisateur pointe dessus avec la souris.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .

L’image par défaut est celle spécifiée dans l’attribut **image** ou sa valeur par défaut.

Si l’image de survol est plus grande que la région définie, l’image de survol est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="examples"></a>Exemples

Consultez *BUTTONELEMENT*. attribut [mappingColor](buttonelement-mappingcolor.md) pour un exemple illustrant l’utilisation de cet attribut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





