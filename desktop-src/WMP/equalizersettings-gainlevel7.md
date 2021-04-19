---
title: EQUALIZERSETTINGS.gainLevel7
description: L’attribut gainLevel7 spécifie ou récupère le niveau de gain de la bande 7.
ms.assetid: f39e1475-b0c8-4204-b2d8-943bc8b4f830
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. gainLevel7
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel7
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ef5177decd983ae8365090caac5c5bbd510b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528446"
---
# <a name="equalizersettingsgainlevel7"></a>EQUALIZERSETTINGS.gainLevel7

L’attribut **gainLevel7** spécifie ou récupère le niveau de gain de la bande 7.

``` syntax
        elementID.gainLevel7
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Notes

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 2kHz.

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

 

 





