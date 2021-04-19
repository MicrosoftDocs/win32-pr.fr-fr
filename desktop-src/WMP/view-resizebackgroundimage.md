---
title: VUE. resizeBackgroundImage
description: L’attribut resizeBackgroundImage spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- AFFICHER. resizeBackgroundImage lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525322"
---
# <a name="viewresizebackgroundimage"></a>VUE. resizeBackgroundImage

L’attribut **resizeBackgroundImage** spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeurs | Description                                      |
|--------|--------------------------------------------------|
| true   | L’image d’arrière-plan peut être redimensionnée.             |
| false  | Par défaut. Impossible de redimensionner l’image d’arrière-plan. |



 

## <a name="remarks"></a>Notes

Si vous affectez à cet attribut la valeur true, l’image d’arrière-plan est redimensionnée pour s’ajuster aux valeurs actuelles des attributs **Width** et **Height** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> <dt>

[**VIEW. backgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 





