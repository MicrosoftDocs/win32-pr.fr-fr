---
title: PLAYLIST. dropDownImage
description: L’attribut dropDownImage spécifie ou récupère le nom de l’image utilisée pour le bouton de liste déroulante qui s’affiche sur le bord droit de la liste déroulante.
ms.assetid: 92454a8a-1688-4b5d-887d-6847f4232d87
keywords:
- PLAYLIST. dropDownImage Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f583fb0cb7b10bd56c19a3863649ac750f5b254a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404165"
---
# <a name="playlistdropdownimage"></a>PLAYLIST. dropDownImage

L’attribut **dropDownImage** spécifie ou récupère le nom de l’image utilisée pour le bouton de liste déroulante qui s’affiche sur le bord droit de la liste déroulante.

``` syntax
        elementID.dropDownImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant le nom d’un fichier image. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Notes

Cet attribut prend en charge les fichiers PNG, JPG, BMP et GIF. Si l’image est un fichier BMP 8 bits, ses valeurs de teinte et de saturation peuvent être modifiées de manière dynamique à l’aide des attributs **hueShift** et **saturation** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. dropDownBackgroundImage**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**PLAYLIST. hueShift**](playlist-hueshift.md)
</dt> <dt>

[**PLAYLIST. saturation**](playlist-saturation.md)
</dt> </dl>

 

 





