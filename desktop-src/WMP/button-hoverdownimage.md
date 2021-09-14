---
title: BUTTON. hoverDownImage
description: L’attribut hoverDownImage spécifie ou récupère l’image affichée lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec le pointeur de la souris.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON. hoverDownImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855778"
---
# <a name="buttonhoverdownimage"></a>BUTTON. hoverDownImage

L’attribut **hoverDownImage** spécifie ou récupère l’image affichée lorsque le **bouton** est à l’état inactif et que l’utilisateur pointe dessus avec le pointeur de la souris.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Notes

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.

L’image par défaut est celle spécifiée dans l’attribut **downImage** ou sa valeur par défaut.

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

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





