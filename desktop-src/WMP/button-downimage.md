---
title: BUTTON. downImage
description: L’attribut downImage spécifie ou récupère l’image représentant l’état inactif du bouton.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON. downImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff24c568ae607b5b67d766f28eb7c221844f1434a959952628cc2ad5a5d6d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123739"
---
# <a name="buttondownimage"></a>BUTTON. downImage

L’attribut **downImage** spécifie ou récupère l’image représentant l’état inactif du **bouton**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Remarques

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.

L’image par défaut est celle spécifiée dans l’attribut **image** ou sa valeur par défaut.

Si l’image inférieure est plus grande que la région définie dans l’attribut ambiant, l’image descendante est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> <dt>

[**BUTTON. suiv.**](button-down.md)
</dt> <dt>

[**BOUTON. image**](button-image.md)
</dt> </dl>

 

 





