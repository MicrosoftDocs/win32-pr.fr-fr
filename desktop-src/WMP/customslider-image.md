---
title: CUSTOMSLIDER. image
description: L’attribut image spécifie ou récupère le nom du fichier contenant les images correspondant aux différents États du curseur personnalisé.
ms.assetid: 7db4f924-76af-4451-831c-1ed8ab1315ee
keywords:
- Lecteur Windows Media CUSTOMSLIDER. image
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f425ce138b2a11d2be834f39603ecc295c52c706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540959"
---
# <a name="customsliderimage"></a>CUSTOMSLIDER. image

L’attribut **image** spécifie ou récupère le nom du fichier contenant les images correspondant aux différents États du curseur personnalisé.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Notes

L’attribut **image** est obligatoire. Il spécifie un fichier image qui se compose d’une ou de plusieurs sous-images, agencées horizontalement ou verticalement, représentant les différents États du curseur personnalisé. Chaque sous-image doit avoir les mêmes dimensions que le **positionImage** ou le curseur personnalisé ne fonctionnera pas correctement. La hauteur ou la largeur de l’image globale doit donc être un multiple pair de la hauteur ou de la largeur du **positionImage**.

Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="examples"></a>Exemples

Voici un exemple d’image de curseur personnalisée. Le **positionImage** correspondant est affiché dans la section exemple de la propriété **positionImage** .

![exemple d’image customslider](images/dial.png)

L’attribut **positionImage** contient également un exemple de code illustrant la façon dont les attributs de l’élément **CUSTOMSLIDER** sont utilisés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER.positionImage**](customslider-positionimage.md)
</dt> </dl>

 

 





