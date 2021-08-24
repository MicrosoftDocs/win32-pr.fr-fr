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
ms.openlocfilehash: 78c3768afd8b1356a1c0ca67a43f951e19143258dfc4f27a3a5e9d861fe9e930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864479"
---
# <a name="buttondisabledimage"></a>BUTTON. disabledImage

L’attribut **disabledImage** spécifie ou récupère l’image qui s’affiche lorsque le **bouton** est désactivé.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom du fichier image.

## <a name="remarks"></a>Remarques

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF.

Cette image s’affiche lorsque l’attribut **désactivé** du contrôle a la valeur true. Si la taille de l’image désactivée est supérieure à celle de la région définie, l’image désactivée est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> </dl>

 

 





