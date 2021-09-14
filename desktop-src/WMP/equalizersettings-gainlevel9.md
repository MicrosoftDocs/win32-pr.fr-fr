---
title: EQUALIZERSETTINGS.gainLevel9
description: L’attribut gainLevel9 spécifie ou récupère le niveau de gain de la bande 9.
ms.assetid: 2bed7486-4d4c-4c71-8bab-8dd0c4f56911
keywords:
- EQUALIZERSETTINGS. gainLevel9 Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel9
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd03197b4d1b6be48b0e91193b3eebfaf28a768
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011009"
---
# <a name="equalizersettingsgainlevel9"></a>EQUALIZERSETTINGS.gainLevel9

L’attribut **gainLevel9** spécifie ou récupère le niveau de gain de la bande 9.

``` syntax
        elementID.gainLevel9
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Notes

Cet attribut ajuste la partie du spectre de fréquences audio centrée sur 8kHz.

Si cet attribut n’est pas spécifié, la valeur précédente est conservée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





