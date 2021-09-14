---
description: Spécifie le niveau de mixage, en décibels (dB), dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Propriété AVEncDDProductionMixLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111857"
---
# <a name="avencddproductionmixlevel-property"></a>Propriété AVEncDDProductionMixLevel

Spécifie le niveau de mixage, en décibels (dB), dans un flux audio Dolby Digital. Cette propriété s’applique aux encodeurs audio Dolby Digital.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncDDProductionMixLevel**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Notes

Si vous définissez cette propriété, affectez la valeur **true** à la propriété [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) .

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

 

 




