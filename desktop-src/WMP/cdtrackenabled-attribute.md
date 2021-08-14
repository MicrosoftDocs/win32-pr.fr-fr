---
title: Attribut CDTrackEnabled
description: L’attribut CDTrackEnabled indique si la piste est activée pour la lecture.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Lecteur Windows Media de l’attribut CDTrackEnabled
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a86c94c2c1b44327cdbfb35544c3e0b5b34d25885215d78dbec0ec084d056e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342682"
---
# <a name="cdtrackenabled-attribute"></a>Attribut CDTrackEnabled

L’attribut **CDTrackEnabled** indique si la piste est activée pour la lecture.

## <a name="applies-to"></a>S'applique à

-   [Pistes de CD](cd-track-attributes.md)

## <a name="remarks"></a>Remarques

Cet attribut est stocké uniquement dans le cache de la bibliothèque.

lors de la lecture d’un CD dans Lecteur Windows Media, l’utilisateur peut sélectionner une piste et spécifier qu’elle ne doit pas être lue. Cette valeur de cet attribut est true si la piste peut être lue, ou false si l’utilisateur a spécifié que la piste ne doit pas être lue.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> </dl>

 

 





