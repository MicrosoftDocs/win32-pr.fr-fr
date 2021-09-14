---
description: Spécifie le type de salle pour un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propriété AVEncDDProductionRoomType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111854"
---
# <a name="avencddproductionroomtype-property"></a>Propriété AVEncDDProductionRoomType

Spécifie le type de salle pour un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .

## <a name="remarks"></a>Notes

Le *type de salle* fait référence à la taille de l’espace utilisé pendant la production. Si vous définissez cette propriété, affectez la valeur **true** à la propriété [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) .

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

 

