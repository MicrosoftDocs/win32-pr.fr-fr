---
title: EFFECTs. fenêtre
description: L’attribut Windowed spécifie ou récupère une valeur indiquant si la visualisation sera affichée ou sans fenêtre, c’est-à-dire si le rectangle entier du contrôle sera visible à tout moment, ou s’il peut être coupé.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFECTs. Windows Media Player avec fenêtres
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534906"
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



 

## <a name="remarks"></a>Notes

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

 

 





