---
title: Attribut UserEffectiveRating
description: L’attribut UserEffectiveRating est l’évaluation calculée par le lecteur Windows Media en fonction de la fréquence à laquelle l’élément a été lu.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Attribut UserEffectiveRating lecteur Windows Media
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540367"
---
# <a name="usereffectiverating-attribute"></a>Attribut UserEffectiveRating

L’attribut **UserEffectiveRating** est l’évaluation calculée par le lecteur Windows Media en fonction de la fréquence à laquelle l’élément a été lu.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Les évaluations des utilisateurs sont représentées par des valeurs entières, comme décrit dans le tableau suivant. Quand vous spécifiez une valeur, utilisez l’une des valeurs de la colonne valeur d’écriture. Lorsque vous récupérez des valeurs, vous pouvez utiliser les plages de la colonne lecture des valeurs pour déterminer le nombre d’étoiles.



| Rating  | Valeur d’écriture | Lecture des valeurs |
|---------|---------------|----------------|
| Absence | 0             | 0              |
| 1 étoile  | 1             | 1 à 12        |
| 2 étoiles | 25            | 13 à 37       |
| 3 étoiles | 50            | 38 à 62       |
| 4 étoiles | 75            | 63 à 86       |
| 5 étoiles | 99            | 87 à 99       |



 

Cet attribut est stocké uniquement dans la bibliothèque.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





