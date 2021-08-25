---
title: EQUALIZERSETTINGS.gainLevel5
description: L’attribut gainLevel5 spécifie ou récupère le niveau de gain de la bande 5.
ms.assetid: 6077a4dc-b9b8-4e00-8b29-14afe5a44321
keywords:
- EQUALIZERSETTINGS. gainLevel5 Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel5
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a075a518eb27bbfe3ac29f8689afca323037373de518d27e95d1724f1c7364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862869"
---
# <a name="equalizersettingsgainlevel5"></a>EQUALIZERSETTINGS.gainLevel5

L’attribut **gainLevel5** spécifie ou récupère le niveau de gain de la bande 5.

``` syntax
        elementID.gainLevel5
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Remarques

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 500Hz.

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

 

 





