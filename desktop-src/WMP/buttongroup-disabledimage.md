---
title: BUTTONGROUP. disabledImage
description: L’attribut disabledImage spécifie ou récupère le nom de l’image représentant l’état désactivé des boutons dans le BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP. disabledImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eeef37bbc25185a64e767f00f9ce17934e8b445327606b552ad69d282e42e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764349"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP. disabledImage

L’attribut **disabledImage** spécifie ou récupère le nom de l’image représentant l’état désactivé des boutons dans le **BUTTONGROUP**.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .

Lorsque l’attribut **Disabled** d’un élément **BUTTONELEMENT** a la valeur true, la région correspondante de **disabledImage** pour le **BUTTONGROUP** est affichée. Si la taille de l’image désactivée est supérieure à celle de la région définie, l’image désactivée est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

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

[**BUTTONGROUP. saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





