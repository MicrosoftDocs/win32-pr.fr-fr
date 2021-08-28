---
description: Spécifie la fréquence d’images sur le flux de sortie de l’encodeur, en images par seconde.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propriété AVEncVideoOutputFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f1e1105ad98564b8d837f35e574be25bcd6cb9506a2adddbc115129fcb65564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540669"
---
# <a name="avencvideooutputframerate-property"></a>Propriété AVEncVideoOutputFrameRate

Spécifie la fréquence d’images sur le flux de sortie de l’encodeur, en images par seconde.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoOutputFrameRate**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un ratio qui définit la fréquence d’images. Les 32 bits supérieurs contiennent le numérateur et les 32 bits inférieurs contiennent le dénominateur. Le tableau suivant présente les fréquences d’images courantes, en images par seconde.



| Fréquence d’images | Proportions      |
|------------|------------|
| 23,97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29,97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59,94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>Remarques

Les applications peuvent définir cette propriété pour spécifier la fréquence d’images de sortie. Les encodeurs peuvent également retourner cette propriété en tant que fonctionnalité. En fonction de l’encodeur, la valeur peut être limitée à la fréquence d’images d’entrée. Si ce n’est pas le cas, l’encodeur est en mesure de convertir la fréquence d’images en interne. Consultez la [**propriété AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

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

 

