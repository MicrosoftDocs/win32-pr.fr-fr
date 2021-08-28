---
title: EQUALIZERSETTINGS.wowLevel
description: L’attribut wowLevel spécifie ou récupère le niveau de l’effet SRS WOW.
ms.assetid: 8f99d7e1-39b9-42be-ab6d-8435ba7022fa
keywords:
- EQUALIZERSETTINGS. wowLevel Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.wowLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ceef9ed737018951478baac1c62571e6cf9b2ff8eb6cf8d1bedc78f068aef60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123639"
---
# <a name="equalizersettingswowlevel"></a>EQUALIZERSETTINGS.wowLevel

L’attribut **wowLevel** spécifie ou récupère le niveau de l’effet SRS WOW.

``` syntax
        elementID.wowLevel
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) compris entre 0 et 100 avec une valeur par défaut de 50.

## <a name="remarks"></a>Remarques

L’effet SRS WOW est un effet d’amélioration audio. Cet attribut est ignoré si **enhancedAudio** est défini sur false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





