---
title: EQUALIZERSETTINGS.truBassLevel
description: L’attribut truBassLevel spécifie ou récupère le niveau TruBass de SRS.
ms.assetid: 9f8c9dbe-d535-42af-8ea7-74fc10526fba
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. truBassLevel
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.truBassLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a262d90b9363f18b20922f92f77960f3b0b882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532509"
---
# <a name="equalizersettingstrubasslevel"></a>EQUALIZERSETTINGS.truBassLevel

L’attribut **truBassLevel** spécifie ou récupère le niveau TRUBASS de SRS.

``` syntax
        elementID.truBassLevel
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) compris entre 0 et 100 avec une valeur par défaut de 50.

## <a name="remarks"></a>Notes

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

 

 





