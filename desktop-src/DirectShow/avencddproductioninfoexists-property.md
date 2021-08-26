---
description: Spécifie l’indicateur d’informations de production audio dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propriété AVEncDDProductionInfoExists (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d0341cf97b4641dc2ece7e93408e527458235620b32b7e25abe583a67c2ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103469"
---
# <a name="avencddproductioninfoexists-property"></a>Propriété AVEncDDProductionInfoExists

Spécifie l’indicateur d’informations de production audio dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Remarques

Si la valeur est **\_ true**, le niveau de mélange et les paramètres de type d’espace sont valides. Spécifiez ces paramètres avec les propriétés [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) et [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .

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

 

 




