---
title: EQUALIZERSETTINGS.gainLevel2
description: L’attribut gainLevel2 spécifie ou récupère le niveau de gain de la bande 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. gainLevel2
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ca8619f4792b509c5c591c84d547fb7408f747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540185"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

L’attribut **gainLevel2** spécifie ou récupère le niveau de gain de la bande 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Notes

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 62Hz.

Si cet attribut n’est pas spécifié, la valeur précédente est conservée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





