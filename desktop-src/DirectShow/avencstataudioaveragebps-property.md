---
description: Retourne le nombre moyen de bits par seconde de l’audio encodé.
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: Propriété AVEncStatAudioAverageBPS (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b43bf329d1d55b41c7849fee7855d322f3ab1622bca013ca5e96cfa4f519db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999859"
---
# <a name="avencstataudioaveragebps-property"></a>Propriété AVEncStatAudioAverageBPS

Retourne le nombre moyen de bits par seconde de l’audio encodé.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatAudioAverageBPS**

## <a name="remarks"></a>Remarques

Cette propriété est disponible une fois l’encodage terminé.

Cette propriété s’applique uniquement à l’encodage VBR (Quality-based bit rate).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




