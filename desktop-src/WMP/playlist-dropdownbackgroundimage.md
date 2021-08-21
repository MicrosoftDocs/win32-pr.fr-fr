---
title: PLAYLIST. dropDownBackgroundImage
description: L’attribut dropDownBackgroundImage spécifie ou récupère le nom de l’image qui s’affiche dans l’arrière-plan de la liste déroulante.
ms.assetid: 40253d82-7178-4f6c-805b-7c1e92ea0636
keywords:
- PLAYLIST. dropDownBackgroundImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47f964e1aaa4b2d22a922d70ea41970b5c1ae667920dbebf49dd5e6cc1d4dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571459"
---
# <a name="playlistdropdownbackgroundimage"></a>PLAYLIST. dropDownBackgroundImage

L’attribut **dropDownBackgroundImage** spécifie ou récupère le nom de l’image qui s’affiche dans l’arrière-plan de la liste déroulante.

``` syntax
        elementID.dropDownBackgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

Cet attribut prend en charge les fichiers PNG, JPG, BMP et GIF. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. dropDownImage**](playlist-dropdownimage.md)
</dt> <dt>

[**PLAYLIST. hueShift**](playlist-hueshift.md)
</dt> <dt>

[**PLAYLIST. saturation**](playlist-saturation.md)
</dt> </dl>

 

 





