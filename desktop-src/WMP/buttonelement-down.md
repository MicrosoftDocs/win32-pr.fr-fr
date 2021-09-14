---
title: BUTTONELEMENT. suiv.
description: L’attribut UpDown spécifie ou récupère une valeur indiquant si l’élément Button est à la position haut ou inférieure.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT. descendant Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855699"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT. suiv.

L’attribut **UpDown** spécifie ou récupère une valeur indiquant si l’élément Button est à la position haut ou inférieure.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                     |
|-------|-----------------------------------------------------------------|
| true  | Indique que le **BUTTONELEMENT** est en position inférieure.        |
| false | Par défaut. Indique que le **BUTTONELEMENT** est en position de haut. |



 

## <a name="remarks"></a>Notes

Pour qu’un élément Button reste à la position inférieure, la fonction **rémanente** doit avoir la valeur true. Par défaut, l’option **rémanent** a la valeur false et toute tentative de définition de **la** valeur true sera ignorée.

Si une valeur non valide est spécifiée, l’état précédent est conservé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT. downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





