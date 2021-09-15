---
title: VIEW. redimensionnable
description: L’attribut redimensionnable récupère une valeur indiquant si la vue peut être redimensionnée.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VIEW. redimensionnable Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518321"
---
# <a name="viewresizable"></a>VIEW. redimensionnable

L’attribut **redimensionnable** récupère une valeur indiquant si la **vue** peut être redimensionnée.

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une valeur **booléenne** en lecture seule avec une valeur par défaut égale à l’attribut **TitleBar** .



| Valeurs | Description             |
|--------|-------------------------|
| true   | La vue peut être redimensionnée.    |
| false  | Impossible de redimensionner la vue. |



 

## <a name="remarks"></a>Notes

S’il n’y a pas de **TitleBar** et, par conséquent, aucune fenêtre ou bordure, vous devez utiliser la méthode **Size** pour redimensionner l’élément **View** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> </dl>

 

 





