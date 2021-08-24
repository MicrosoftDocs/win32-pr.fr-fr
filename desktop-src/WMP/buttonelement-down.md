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
ms.openlocfilehash: ff20aebda01b24dc14eb7d5298ee0d663d903bedcb7ef6ef8b05b6211af8b567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764469"
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



 

## <a name="remarks"></a>Remarques

Pour qu’un élément Button reste à la position inférieure, la fonction **rémanente** doit avoir la valeur true. Par défaut, l’option **rémanent** a la valeur false et toute tentative de définition de **la** valeur true sera ignorée.

Si une valeur non valide est spécifiée, l’état précédent est conservé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONELEMENT**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT. downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





