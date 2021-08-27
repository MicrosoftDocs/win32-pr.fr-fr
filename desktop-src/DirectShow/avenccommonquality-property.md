---
description: Spécifie le niveau de qualité pour l’encodage.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propriété AVEncCommonQuality (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99202391e919fa1da9028a15a57154834feddd3039160b9b0562a713fe59ddaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087669"
---
# <a name="avenccommonquality-property"></a>Propriété AVEncCommonQuality

Spécifie le niveau de qualité pour l’encodage.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est comprise dans la plage suivante.



| Valeur | Description                           |
|-------|---------------------------------------|
| 0     | Qualité minimale, taille de sortie inférieure. |
| 100   | Qualité maximale, taille de sortie supérieure.  |



 

## <a name="remarks"></a>Remarques

Cette propriété contrôle le niveau de qualité lorsque l’encodeur n’utilise pas une vitesse de transmission avec restriction. La propriété [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) détermine si la vitesse de transmission est restreinte.

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

 

 




