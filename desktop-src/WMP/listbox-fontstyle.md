---
title: LISTBOX. fontStyle
description: L’attribut fontStyle spécifie ou récupère le style de police pour le contrôle de zone de liste.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX. fontStyle lecteur Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527304"
---
# <a name="listboxfontstyle"></a>LISTBOX. fontStyle

L’attribut **FontStyle** spécifie ou récupère le style de police pour le contrôle de zone de liste.

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

[**Élément LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX. FontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





