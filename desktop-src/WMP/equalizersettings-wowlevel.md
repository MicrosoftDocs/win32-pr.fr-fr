---
title: EQUALIZERSETTINGS.wowLevel
description: L’attribut wowLevel spécifie ou récupère le niveau de l’effet SRS WOW.
ms.assetid: 8f99d7e1-39b9-42be-ab6d-8435ba7022fa
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. wowLevel
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.wowLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41d3994e8242ef6194ee0dbf3e395aa055727b81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532597"
---
# <a name="equalizersettingswowlevel"></a>EQUALIZERSETTINGS.wowLevel

L’attribut **wowLevel** spécifie ou récupère le niveau de l’effet SRS WOW.

``` syntax
        elementID.wowLevel
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) compris entre 0 et 100 avec une valeur par défaut de 50.

## <a name="remarks"></a>Notes

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

 

 





