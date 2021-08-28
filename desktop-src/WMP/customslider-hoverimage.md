---
title: CUSTOMSLIDER.hoverImage
description: L’attribut hoverImage spécifie ou récupère l’image qui apparaît lorsque la souris se trouve sur le curseur personnalisé.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- CUSTOMSLIDER. hoverImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d12f337c8d4889e0d2e94bac0c0a4dce74f3a80fda9261d245b91ce5612754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651399"
---
# <a name="customsliderhoverimage"></a>CUSTOMSLIDER.hoverImage

L’attribut **hoverImage** spécifie ou récupère l’image qui apparaît lorsque la souris se trouve sur le curseur personnalisé.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. S’il n’est pas spécifié, le fichier spécifié dans l’attribut **image** sera utilisé.

**HoverImage** représente l’état de survol du contrôle CUSTOMSLIDER ; autrement dit, l’État qui est affiché lorsque le curseur de la souris pointe dessus. Il peut s’agir d’une image unique ou d’une série d’images représentant les différents États du curseur. Si plusieurs images sont utilisées, elles sont organisées de la même façon que le fichier **image** .

Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. image**](customslider-image.md)
</dt> </dl>

 

 





