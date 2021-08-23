---
title: EFFECTs. fenêtre
description: L’attribut Windowed spécifie ou récupère une valeur indiquant si la visualisation sera affichée ou sans fenêtre, c’est-à-dire si le rectangle entier du contrôle sera visible à tout moment, ou s’il peut être coupé.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- effects. windowed Lecteur Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32fcd144d26de8f96c039d8199af8e6e4c1c14e60b2c5e2bf0c7dcc5a7f3cbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650999"
---
# <a name="effectswindowed"></a>EFFECTs. fenêtre

L’attribut **Windowed** spécifie ou récupère une valeur indiquant si la visualisation sera affichée ou sans fenêtre, c’est-à-dire si le rectangle entier du contrôle sera visible à tout moment, ou s’il peut être coupé. Cet attribut ne peut être défini qu’au moment de la conception.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** spécifiée au moment de la conception et en lecture seule par la suite.



| Valeur | Description                              |
|-------|------------------------------------------|
| true  | Le contrôle sera fenêtre.            |
| false | Par défaut. Le contrôle ne sera pas sans fenêtre. |



 

## <a name="remarks"></a>Remarques

Si vous souhaitez une fenêtre de visualisation non rectangulaire ou si une partie de la fenêtre est couverte par une image, cet attribut doit avoir la valeur false. Cela sacrifie certaines performances pour effectuer l’écrêtage nécessaire.

Si **Windowed** a la valeur true, toute image qui recouvre la fenêtre de visualisation est ignorée et la fenêtre de visualisation a l’ordre de plan le plus haut niveau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> </dl>

 

 





