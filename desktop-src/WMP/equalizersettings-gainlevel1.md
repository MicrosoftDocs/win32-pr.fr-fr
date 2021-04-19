---
title: EQUALIZERSETTINGS.gainLevel1
description: L’attribut gainLevel1 spécifie ou récupère le niveau de gain de la bande 1.
ms.assetid: 3d681ade-3fd4-432d-ae92-c083d927346f
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. gainLevel1
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel1
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3299c2b9275eabb4812c83670f28bcbb3d2aeef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534811"
---
# <a name="equalizersettingsgainlevel1"></a>EQUALIZERSETTINGS.gainLevel1

L’attribut **gainLevel1** spécifie ou récupère le niveau de gain de la bande 1.

``` syntax
        elementID.gainLevel1
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Notes

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 31Hz.

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

 

 





