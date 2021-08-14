---
title: EQUALIZERSETTINGS.gainLevel2
description: L’attribut gainLevel2 spécifie ou récupère le niveau de gain de la bande 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- EQUALIZERSETTINGS. gainLevel2 Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4979cb44fbd39b37acd29fe8e3303c879c45b40dfafc554180dad5301f0b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339829"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

L’attribut **gainLevel2** spécifie ou récupère le niveau de gain de la bande 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Remarques

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

 

 





