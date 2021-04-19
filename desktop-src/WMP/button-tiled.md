---
title: BOUTON. en mosaïque
description: L’attribut tileed spécifie ou récupère une valeur indiquant si l’image du bouton sera affichée en mosaïque.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BUTTON. lecteur Windows Media en mosaïque
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541534"
---
# <a name="buttontiled"></a>BOUTON. en mosaïque

L’attribut **tileed** spécifie ou récupère une valeur indiquant si l’image du **bouton** sera affichée en mosaïque.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                       |
|-------|-----------------------------------|
| true  | L’image sera affichée en mosaïque.              |
| false | Par défaut. L’image ne sera pas affichée en mosaïque. |



 

## <a name="remarks"></a>Notes

Si l’image est plus petite que la région réelle du contrôle, la mosaïque de l’image se répète jusqu’à ce qu’elle remplisse toute la région. Si une image n’est pas spécifiée ou ne peut pas être récupérée, la **mosaïque** est définie sur false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> <dt>

[**BOUTON. image**](button-image.md)
</dt> </dl>

 

 





