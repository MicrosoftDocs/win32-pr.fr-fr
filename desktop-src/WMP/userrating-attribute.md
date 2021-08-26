---
title: Attribut UserRating
description: L’attribut UserRating est l’évaluation spécifiée par l’utilisateur dans la bibliothèque.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Lecteur Windows Media de l’attribut UserRating
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41725119f97e0609931a3c9b7789e86d16a20507523e76a3f5642a0955998d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001649"
---
# <a name="userrating-attribute"></a>Attribut UserRating

L’attribut **UserRating** est l’évaluation spécifiée par l’utilisateur dans la bibliothèque.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Sélections](playlist-attributes-ref.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Remarques

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
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure (l’élément photo est pris en charge uniquement dans Lecteur Windows Media 10 ou version ultérieure)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





