---
title: EQUALIZERSETTINGS.gainLevel8
description: L’attribut gainLevel8 spécifie ou récupère le niveau de gain de la bande 8.
ms.assetid: 1cd4fa26-ed9b-4312-8272-9fe8011658e8
keywords:
- EQUALIZERSETTINGS. gainLevel8 Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel8
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92398b8e01e4ad10971cbe19454fed52b0cb0b4f88565e78e597ef4eacdfc1d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736369"
---
# <a name="equalizersettingsgainlevel8"></a>EQUALIZERSETTINGS.gainLevel8

L’attribut **gainLevel8** spécifie ou récupère le niveau de gain de la bande 8.

``` syntax
        elementID.gainLevel8
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Remarques

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 4kHz.

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

 

 





