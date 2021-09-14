---
title: CUSTOMSLIDER.disabledImage
description: L’attribut disabledImage spécifie ou récupère l’image du curseur utilisé lorsque le curseur est désactivé.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- CUSTOMSLIDER. disabledImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228462"
---
# <a name="customsliderdisabledimage"></a>CUSTOMSLIDER.disabledImage

L’attribut **disabledImage** spécifie ou récupère l’image du curseur utilisé lorsque le curseur est désactivé.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image.

## <a name="remarks"></a>Notes

Cet attribut est facultatif. S’il n’est pas spécifié, le fichier spécifié dans l’attribut **image** sera utilisé.

**DisabledImage** représente l’état désactivé du contrôle **CUSTOMSLIDER** . Il peut s’agir d’une image unique ou d’une série d’images représentant les différents États du curseur. Si plusieurs images sont utilisées, elles sont organisées de la même façon que le fichier **image** .

Les types de fichiers image pris en charge sont BMP, JPG, PNG et GIF (à l’exclusion des GIF animés).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. image**](customslider-image.md)
</dt> </dl>

 

 





