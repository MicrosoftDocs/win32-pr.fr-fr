---
title: TEXT. hoverFontStyle
description: L’attribut hoverFontStyle spécifie ou récupère le style de police utilisé pour le contrôle de texte lorsque le curseur de la souris pointe dessus.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- TEXT. hoverFontStyle Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04f2ae8e4231ca89f37a65e591271f2536679da649d1efd22ffc1063c89d17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134622"
---
# <a name="texthoverfontstyle"></a>TEXT. hoverFontStyle

L’attribut **hoverFontStyle** spécifie ou récupère le style de police utilisé pour le contrôle de texte lorsque le curseur de la souris pointe dessus.

``` syntax
        elementID.hoverFontStyle
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

Si **hoverFontStyle** n’est pas spécifié, **FontStyle** est utilisé.

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

 

 





