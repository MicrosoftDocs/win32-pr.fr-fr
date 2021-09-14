---
title: BUTTON. hoverImage
description: L’attribut hoverImage spécifie ou récupère l’image affichée lorsque le bouton est à l’État haut et que l’utilisateur place le pointeur de la souris sur celui-ci.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON. hoverImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855766"
---
# <a name="buttonhoverimage"></a>BUTTON. hoverImage

L’attribut **hoverImage** spécifie ou récupère l’image affichée lorsque le **bouton** est à l’État haut et que l’utilisateur place le pointeur de la souris sur celui-ci.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Notes

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.

L’image par défaut est celle spécifiée dans l’attribut **image** ou sa valeur par défaut.

Si l’image de survol est plus grande que la région définie dans l’attribut ambiant, l’image de survol est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> <dt>

[**BOUTON. image**](button-image.md)
</dt> </dl>

 

 





