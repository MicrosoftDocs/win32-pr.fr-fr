---
title: Attribut MediaContentTypes
description: L’attribut MediaContentTypes spécifie le type de contenu dans l’élément.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Attribut MediaContentTypes lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530304"
---
# <a name="mediacontenttypes-attribute"></a>Attribut MediaContentTypes

L’attribut **MediaContentTypes** spécifie le type de contenu dans l’élément.

## <a name="applies-to"></a>S'applique à

-   [Sélections](playlist-attributes-ref.md)

## <a name="remarks"></a>Notes

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

 

 





