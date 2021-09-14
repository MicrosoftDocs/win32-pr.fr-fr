---
description: Active ou désactive l’accélération matérielle pour le décodage vidéo VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: AVDecVideoAcceleration_VC1, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112061"
---
# <a name="avdecvideoacceleration_vc1-property"></a>AVDecVideoAcceleration \_ propriété VC1

Active ou désactive l’accélération matérielle pour le décodage vidéo VC-1.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Notes

Si la valeur est égale à zéro, le décodeur n’utilise pas DirectX Video Acceleration (DXVA) pour le décodage vidéo VC-1. pour les filtres de DirectShow, définissez cette propriété avant que la broche de sortie du décodeur soit connectée.

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

 

 




