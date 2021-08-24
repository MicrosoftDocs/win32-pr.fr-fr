---
title: TEXT. disabledFontStyle
description: L’attribut disabledFontStyle spécifie ou récupère le style de police utilisé pour le contrôle Text lorsqu’il est désactivé.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- TEXT. disabledFontStyle Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0119139e481eee6673c61f95425eac0a3918d738c3d18278442ba7713718b7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507589"
---
# <a name="textdisabledfontstyle"></a>TEXT. disabledFontStyle

L’attribut **disabledFontStyle** spécifie ou récupère le style de police utilisé pour le contrôle Text lorsqu’il est désactivé.

``` syntax
        elementID.disabledFontStyle
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



 

## <a name="remarks"></a>Remarques

Vous pouvez utiliser n’importe quelle combinaison de valeurs, en les séparant par des espaces. Le style normal est prioritaire sur toutes les autres valeurs, et les autres valeurs spécifiées en même temps que normal seront ignorées.

Si **disabledFontStyle** n’est pas spécifié, **FontStyle** est utilisé.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





