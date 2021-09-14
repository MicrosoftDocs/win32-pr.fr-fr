---
description: Spécifie la coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique sur un flux audio Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Propriété AVDecDDDynamicRangeScaleHigh (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112089"
---
# <a name="avdecdddynamicrangescalehigh-property"></a>Propriété AVDecDDDynamicRangeScaleHigh

Spécifie la coupe de haut niveau lorsque le décodeur effectue un contrôle de plage dynamique sur un flux audio Dolby AC-3.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est comprise dans la plage suivante.



| Valeur | Description                                                    |
|-------|----------------------------------------------------------------|
| 0     | Aucune compression de plage dynamique. Conserver la plage dynamique complète. |
| 100   | Appliquez la compression de plage dynamique complète.                          |



 

## <a name="remarks"></a>Notes

Cette propriété s’applique uniquement lorsque la valeur de la propriété [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) est eAVDecDDOperationalMode \_ .

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

 

 




