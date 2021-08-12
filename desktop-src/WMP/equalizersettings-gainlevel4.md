---
title: EQUALIZERSETTINGS.gainLevel4
description: L’attribut gainLevel4 spécifie ou récupère le niveau de gain de la bande 4.
ms.assetid: 01383171-f991-4d09-858a-ce21ce93e14e
keywords:
- EQUALIZERSETTINGS. gainLevel4 Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b1479d1be95895f124c5150d17a281fec5fc95fcbbedd65ca2ce9887678fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578165"
---
# <a name="equalizersettingsgainlevel4"></a>EQUALIZERSETTINGS.gainLevel4

L’attribut **gainLevel4** spécifie ou récupère le niveau de gain de la bande 4.

``` syntax
        elementID.gainLevel4
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Notes

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 250Hz.

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

 

 





