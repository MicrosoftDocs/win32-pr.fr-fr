---
title: Attribut UserServiceRating
description: L’attribut UserServiceRating est réservé pour une utilisation ultérieure.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Lecteur Windows Media de l’attribut UserServiceRating
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1dc9b0f1131a02a4ce3fe05ebe2423116e7701e3bbb9ce7f5ea8faa1c1dce7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001589"
---
# <a name="userservicerating-attribute"></a>Attribut UserServiceRating

L’attribut **UserServiceRating** est réservé pour une utilisation ultérieure.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
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
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





