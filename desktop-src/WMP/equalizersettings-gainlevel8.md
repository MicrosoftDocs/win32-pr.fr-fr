---
title: EQUALIZERSETTINGS.gainLevel8
description: L’attribut gainLevel8 spécifie ou récupère le niveau de gain de la bande 8.
ms.assetid: 1cd4fa26-ed9b-4312-8272-9fe8011658e8
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. gainLevel8
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel8
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 814f22a94d1e69c2d101154c6f4a3984a67bd75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530297"
---
# <a name="equalizersettingsgainlevel8"></a>EQUALIZERSETTINGS.gainLevel8

L’attribut **gainLevel8** spécifie ou récupère le niveau de gain de la bande 8.

``` syntax
        elementID.gainLevel8
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20. Sa valeur par défaut est zéro.

## <a name="remarks"></a>Notes

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

 

 





