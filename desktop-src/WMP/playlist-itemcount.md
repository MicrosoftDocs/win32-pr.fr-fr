---
title: PLAYLIST. itemCount
description: L’attribut itemCount récupère le nombre d’éléments actuellement affichés dans l’élément PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- PLAYLIST. itemCount lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528829"
---
# <a name="playlistitemcount"></a>PLAYLIST. itemCount

L’attribut **ItemCount** récupère le nombre d’éléments actuellement affichés dans l’élément **playlist** .

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture seule (**long**).

## <a name="remarks"></a>Notes

La propriété **ItemCount** compte le nombre total d’éléments développés. Par exemple, s’il existe deux sélections contenant chacune trois éléments multimédias, **ItemCount** retourne 2 si les sélections ne sont pas développées. Si seule la première sélection est développée, **ItemCount** retourne 4. Si les deux sélections sont développées, **ItemCount** retourne 6.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





