---
title: BUTTON. disabledImage
description: L’attribut disabledImage spécifie ou récupère l’image qui s’affiche lorsque le bouton est désactivé.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON. disabledImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855813"
---
# <a name="buttondisabledimage"></a>BUTTON. disabledImage

L’attribut **disabledImage** spécifie ou récupère l’image qui s’affiche lorsque le **bouton** est désactivé.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Notes

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.

Cette image s’affiche lorsque l’attribut **désactivé** du contrôle a la valeur true. Si la taille de l’image désactivée est supérieure à celle de la région définie, l’image désactivée est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> </dl>

 

 





