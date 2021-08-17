---
title: CUSTOMSLIDER.downImage
description: L’attribut downImage spécifie ou récupère l’image de l’état inactif du curseur personnalisé.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- CUSTOMSLIDER. downImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e151f825dab7170c3e3678f280303265af0df91561c7dc709323dd8043809e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750338"
---
# <a name="customsliderdownimage"></a>CUSTOMSLIDER.downImage

L’attribut **downImage** spécifie ou récupère l’image de l’état inactif du curseur personnalisé.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Remarques

Cet attribut est facultatif. S’il n’est pas spécifié, le fichier spécifié dans l’attribut **image** sera utilisé.

**DownImage** représente l’état inactif du contrôle **CUSTOMSLIDER** . Il peut s’agir d’une image unique ou d’une série d’images représentant les différents États du curseur. Si plusieurs images sont utilisées, elles sont organisées de la même façon que le fichier **image** .

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

 

 





