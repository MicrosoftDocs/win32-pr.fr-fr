---
title: EQUALIZERSETTINGS.truBassLevel
description: L’attribut truBassLevel spécifie ou récupère le niveau TruBass de SRS.
ms.assetid: 9f8c9dbe-d535-42af-8ea7-74fc10526fba
keywords:
- EQUALIZERSETTINGS. truBassLevel Lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.truBassLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17fdb293ee081c99055a88fcd8a6ffeb420c9eb922be655f92df04c71058af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901949"
---
# <a name="equalizersettingstrubasslevel"></a>EQUALIZERSETTINGS.truBassLevel

L’attribut **truBassLevel** spécifie ou récupère le niveau TRUBASS de SRS.

``` syntax
        elementID.truBassLevel
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) compris entre 0 et 100 avec une valeur par défaut de 50.

## <a name="remarks"></a>Remarques

TruBass est un effet qui améliore le son des niveaux de basses de la piste audio. Cet attribut est ignoré si **enhancedAudio** est défini sur false.

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

 

 





