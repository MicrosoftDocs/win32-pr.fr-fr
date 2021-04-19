---
title: Attribut CDTrackEnabled
description: L’attribut CDTrackEnabled indique si la piste est activée pour la lecture.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Attribut CDTrackEnabled lecteur Windows Media
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541755"
---
# <a name="cdtrackenabled-attribute"></a>Attribut CDTrackEnabled

L’attribut **CDTrackEnabled** indique si la piste est activée pour la lecture.

## <a name="applies-to"></a>S'applique à

-   [Pistes de CD](cd-track-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut est stocké uniquement dans le cache de la bibliothèque.

Lors de la lecture d’un CD dans le lecteur Windows Media, l’utilisateur peut sélectionner une piste et spécifier qu’elle ne doit pas être lue. Cette valeur de cet attribut est true si la piste peut être lue, ou false si l’utilisateur a spécifié que la piste ne doit pas être lue.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





