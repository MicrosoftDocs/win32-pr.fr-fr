---
title: BUTTONGROUP. hoverDownImage
description: L’attribut hoverDownImage spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le BUTTONGROUP. L’état Survol se produit lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec la souris.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP. hoverDownImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84d907a9b3fd1fc1a2eaf2dcf30337d016ae0732b147f435f49343d791b65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119878"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP. hoverDownImage

L’attribut **hoverDownImage** spécifie ou récupère le nom de l’image représentant l’état de survol d’un bouton dans le **BUTTONGROUP**. L’état Survol se produit lorsque le bouton est à l’état inactif et que l’utilisateur pointe dessus avec la souris.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Les formats d’image pris en charge sont BMP, JPG, PNG et GIF. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .

L’image par défaut est celle spécifiée dans l’attribut **downImage** ou sa valeur par défaut.

Si l’image de survol est plus grande que la région définie, l’image de survol est rognée.

Si l’image ne peut pas être récupérée, une image par défaut (l’image rouge-x) s’affiche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP. hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





