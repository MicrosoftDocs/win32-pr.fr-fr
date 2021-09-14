---
description: Spécifie l’indicateur d’informations de production audio dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propriété AVEncDDProductionInfoExists (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111858"
---
# <a name="avencddproductioninfoexists-property"></a>Propriété AVEncDDProductionInfoExists

Spécifie l’indicateur d’informations de production audio dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Notes

Si la valeur est **\_ true**, le niveau de mélange et les paramètres de type d’espace sont valides. Spécifiez ces paramètres avec les propriétés [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) et [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .

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

 

 




