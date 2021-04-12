---
description: Spécifie le niveau de qualité pour l’encodage.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Propriété AVEncCommonQuality (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482512"
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



 

## <a name="remarks"></a>Notes

Cette propriété contrôle le niveau de qualité lorsque l’encodeur n’utilise pas une vitesse de transmission avec restriction. La propriété [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) détermine si la vitesse de transmission est restreinte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




