---
title: BUTTON. suiv.
description: L’attribut UpDown spécifie ou récupère une valeur indiquant si le bouton se trouve à la position haut ou inférieure.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BUTTON. vers le lecteur Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539699"
---
# <a name="buttondown"></a>BUTTON. suiv.

L’attribut **UpDown** spécifie ou récupère une valeur indiquant si le **bouton** se trouve à la position haut ou inférieure.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                   |
|-------|---------------------------------------------------------------|
| true  | Indique que le **bouton** est en position inférieure.        |
| false | Par défaut. Indique que le **bouton** se trouve à la position de haut. |



 

## <a name="remarks"></a>Notes

Pour qu’un **bouton** reste à la position inférieure, l’option **rémanent** doit avoir la valeur true. Par défaut, l’option **rémanent** a la valeur false et toute tentative de définition de **la** valeur true sera ignorée.

Si une valeur non valide est spécifiée, l’état précédent est conservé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> <dt>

[**BUTTON. downToolTip**](button-downtooltip.md)
</dt> </dl>

 

 





