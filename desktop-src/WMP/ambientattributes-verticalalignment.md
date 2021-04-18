---
title: AmbientAttributes. verticalAlignment
description: L’attribut verticalAlignment spécifie ou récupère une valeur indiquant le positionnement vertical du contrôle lorsque la vue ou la sous-vue parente est étirée.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- Lecteur Windows Media AmbientAttributes. verticalAlignment
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88de2f5f54b95b14827fabb2bafb89ff6974966b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540652"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes. verticalAlignment

L’attribut **VerticalAlignment** spécifie ou récupère une valeur indiquant le positionnement vertical du contrôle lorsque la **vue** ou la sous- **vue** parente est étirée.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.



| Valeur   | Description                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Par défaut. Maintient le positionnement du contrôle par rapport au haut de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.                                                                                                                                                                                                             |
| bottom  | Maintient le positionnement du contrôle par rapport au bas de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.                                                                                                                                                                                                                   |
| centre  | Maintient le positionnement du contrôle par rapport au centre vertical de la **vue** ou de la sous- **vue** parente lorsque la vue est redimensionnée.                                                                                                                                                                                                          |
| étirement | Maintient la position du contrôle par rapport aux marges supérieure et inférieure de la vue lors du redimensionnement. Le contrôle s’étire pour s’ajuster lorsque la **vue** ou la sous- **vue** parente est étirée. L’image réelle n’est pas agrandie ou réduite, à moins qu’elle ne soit redimensionnable, mais la zone cliquable augmente ou diminue si elle n’est pas limitée par un **clippingImage**. |



 

## <a name="remarks"></a>Notes

À moins que **VerticalAlignment** ne soit défini sur « Center », le contrôle conserve sa distance d’origine à partir du bord spécifié, ou à partir des deux bords si « Stretch » est spécifié et que le contrôle est redimensionnable. Si le contrôle n’est pas redimensionnable et que « Stretch » est spécifié, la zone cliquable est étirée à la place.

Vous pouvez définir n’importe quelle combinaison d’attributs **HorizontalAlignment** et **VerticalAlignment** . Par exemple, si vous souhaitez qu’un contrôle soit centré à la fois horizontalement et verticalement, définissez **HorizontalAlignment** sur « Center » et **VerticalAlignment** sur « Center ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





