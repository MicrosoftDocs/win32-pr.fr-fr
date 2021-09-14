---
description: Définit le seuil auquel l’encodeur considère un champ vidéo redondant.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Propriété AVEncVideoInverseTelecineThreshold (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111585"
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



 

## <a name="remarks"></a>Notes

Définissez cette propriété si l’encodeur effectue un télécinéma inverse avec une source vidéo analogique.

## <a name="requirements"></a>Spécifications



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

 

 




