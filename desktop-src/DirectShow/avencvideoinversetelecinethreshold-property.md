---
description: Définit le seuil auquel l’encodeur considère un champ vidéo redondant.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propriété AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297dae601c5112714272a2d1c2e0b1a7ebeee5faa3aa2fabebc32e79c1745c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275178"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>Propriété AVEncVideoInverseTelecineThreshold

Définit le seuil auquel l’encodeur considère un champ vidéo redondant.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est comprise dans la plage suivante.



| Valeur | Description                                                    |
|-------|----------------------------------------------------------------|
| 0     | L’encodeur est moins susceptible de considérer les champs vidéo comme redondants. |
| 100   | L’encodeur est plus susceptible de considérer les champs vidéo comme redondants. |



 

## <a name="remarks"></a>Remarques

Définissez cette propriété si l’encodeur effectue un télécinéma inverse avec une source vidéo analogique.

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

 

 




