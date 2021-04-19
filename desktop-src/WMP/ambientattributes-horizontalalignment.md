---
title: AmbientAttributes. horizontalAlignment
description: L’attribut horizontalAlignment spécifie ou récupère une valeur qui indique le positionnement horizontal du contrôle lorsque la vue ou la sous-vue parente est redimensionnée.
ms.assetid: 97ca23b9-2046-45ee-b2da-ea388e7ab8d8
keywords:
- Lecteur Windows Media AmbientAttributes. horizontalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.horizontalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f946f0d095526c9fc0894cdf0270cbf7cc0c81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537330"
---
# <a name="ambientattributeshorizontalalignment"></a>AmbientAttributes. horizontalAlignment

L’attribut **HorizontalAlignment** spécifie ou récupère une valeur qui indique le positionnement horizontal du contrôle lorsque la **vue** ou la sous- **vue** parente est redimensionnée.

``` syntax
        elementID.horizontalAlignment
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



| Valeur   | Description                                                                                                                                                                                                                                                                                                                                                        |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| gauche    | Par défaut. Maintient le positionnement du contrôle par rapport à la gauche de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.                                                                                                                                                                                                                               |
| droite   | Maintient le positionnement du contrôle par rapport à la droite de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.                                                                                                                                                                                                                                       |
| centre  | Maintient le positionnement du contrôle par rapport au centre horizontal de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.                                                                                                                                                                                                                           |
| étirement | Maintient le positionnement du contrôle par rapport aux marges gauche et droite de la **vue** ou de la sous- **vue** parente lors du redimensionnement. Le contrôle s’étire pour s’ajuster lorsque la **vue** ou la sous- **vue** est étirée. L’image réelle n’est pas agrandie ou réduite, à moins qu’elle ne soit redimensionnable, mais la zone cliquable augmente ou diminue si elle n’est pas limitée par un **clippingImage**. |



 

## <a name="remarks"></a>Notes

Sauf si **HorizontalAlignment** est défini sur « Center », le contrôle conserve sa distance d’origine à partir du bord spécifié, ou des deux bords si « Stretch » est spécifié et que le contrôle est redimensionnable. Si le contrôle n’est pas redimensionnable et que « Stretch » est spécifié, la zone cliquable est étirée à la place.

Vous pouvez définir n’importe quelle combinaison de **HorizontalAlignment** et **VerticalAlignment**. Par exemple, si vous souhaitez centrer un contrôle à la fois horizontalement et verticalement, définissez horizontalAlignment = "Center" verticalAlignment = "Center".

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. verticalAlignment**](ambientattributes-verticalalignment.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> </dl>

 

 





