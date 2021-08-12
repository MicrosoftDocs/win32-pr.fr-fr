---
title: EDITBOX. fontStyle
description: L’attribut fontStyle spécifie ou récupère le style de police pour le contrôle zone d’édition.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EDITBOX. fontStyle Lecteur Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d9dc5ac5fe3750fb3a6af8658a5ddb30274764cc891438162434a44651322a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578845"
---
# <a name="editboxfontstyle"></a>EDITBOX. fontStyle

L’attribut **FontStyle** spécifie ou récupère le style de police pour le contrôle zone d’édition.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant une ou plusieurs des valeurs suivantes.



| Valeur     | Description           |
|-----------|-----------------------|
| Gras      | Style de police gras.      |
| Italique    | Style de police en italique.    |
| Souligner | Style de police souligné. |
| Barré | Style de police barré. |
| Normal    | Style de police normal.    |



 

## <a name="remarks"></a>Notes

Vous pouvez utiliser n’importe quelle combinaison de valeurs, en les séparant par des espaces. Le style normal est prioritaire sur toutes les autres valeurs, et les autres valeurs spécifiées en même temps que normal seront ignorées.

À des fins de rendu, normal est le style de police par défaut. La valeur par défaut Récupérée à partir de cet attribut est "" (chaîne vide).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. fontFace**](editbox-fontface.md)
</dt> <dt>

[**EDITBOX. FontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





