---
title: TEXT. fontStyle
description: L’attribut fontStyle spécifie ou récupère le style de police pour le contrôle de texte.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545366"
---
# <a name="textfontstyle"></a>TEXT. fontStyle

L’attribut **FontStyle** spécifie ou récupère le style de police pour le contrôle de texte.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture contenant une ou plusieurs des valeurs suivantes.



| Valeur     | Description                 |
|-----------|-----------------------------|
| Gras      | Style de police gras.            |
| Italique    | Style de police en italique.          |
| Souligner | Style de police souligné.       |
| Barré | Style de police barré.       |
| Normal    | Par défaut. Style de police normal. |



 

## <a name="remarks"></a>Notes

Vous pouvez utiliser n’importe quelle combinaison de valeurs, en les séparant par des espaces. Le style normal est prioritaire sur toutes les autres valeurs, et les autres valeurs spécifiées en même temps que normal seront ignorées.

Pour obtenir un exemple illustrant l’utilisation des attributs de l’élément de **texte** , consultez l’attribut [value](text-value.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément de texte**](text-element.md)
</dt> </dl>

 

 





