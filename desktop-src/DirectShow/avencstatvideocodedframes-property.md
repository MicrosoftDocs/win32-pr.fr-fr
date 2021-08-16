---
description: Retourne le nombre de trames vidéo qui ont été encodées.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propriété AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f8858aba7a36d79096eccad40990e1859d4073695aaf80910587bac4005d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342559"
---
# <a name="avencstatvideocodedframes-property"></a>Propriété AVEncStatVideoCodedFrames

Retourne le nombre de trames vidéo qui ont été encodées.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Remarques

Cette propriété est disponible une fois l’encodage terminé.

La valeur de cette propriété est égale à la propriété [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) moins le nombre de frames supprimés. L’encodeur peut supprimer des frames pour rester dans les limites de la vitesse de transmission spécifiée. Elle peut également supprimer des frames à la fin du flux (consultez la propriété [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).

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

 

 




