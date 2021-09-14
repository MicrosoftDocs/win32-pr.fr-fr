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
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191803"
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

## <a name="requirements"></a>Spécifications



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

 

 





