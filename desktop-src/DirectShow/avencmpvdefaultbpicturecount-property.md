---
description: Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.
ms.assetid: d41ed713-0159-4325-bc44-f4a3eea10aa2
title: Propriété AVEncMPVDefaultBPictureCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95604d8b3849175e579d276fa006f5a8c4d2833a167228316c4cf830b01618b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276259"
---
# <a name="avencmpvdefaultbpicturecount-property"></a>Propriété AVEncMPVDefaultBPictureCount

Spécifie le nombre par défaut de frames B consécutifs entre I et P frames.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPVDefaultBPictureCount**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Remarques

avant Windows 8, cette propriété s’applique aux encodeurs vidéo MPEG. à partir de Windows 8, cette propriété est utilisée par les encodeurs vidéo MPEG, WMV et H. 264.

Si l’encodeur prend en charge cette propriété, il peut être utilisé pour contrôler la structure du groupe d’images (GOP).

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

 

 




