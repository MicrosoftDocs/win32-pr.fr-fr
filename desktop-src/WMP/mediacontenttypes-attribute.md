---
title: Attribut MediaContentTypes
description: L’attribut MediaContentTypes spécifie le type de contenu dans l’élément.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Lecteur Windows Media de l’attribut MediaContentTypes
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca3c422083954554db76657a0bb9cc10062fd878a9ebf4b31f4dc88734ac1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996239"
---
# <a name="mediacontenttypes-attribute"></a>Attribut MediaContentTypes

L’attribut **MediaContentTypes** spécifie le type de contenu dans l’élément.

## <a name="applies-to"></a>S'applique à

-   [Sélections](playlist-attributes-ref.md)

## <a name="remarks"></a>Remarques

Cet attribut peut prendre l’une des valeurs suivantes :



| Valeur | Signification                                |
|-------|----------------------------------------|
| 1     | La sélection contient du contenu audio.   |
| 2     | À fournir.                        |
| 3     | La sélection contient du contenu audio.   |
| 4     | La sélection contient du contenu vidéo.   |
| 5     | La sélection contient le contenu de l’image. |
| 6     | La sélection contient du contenu TV.      |



 

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





