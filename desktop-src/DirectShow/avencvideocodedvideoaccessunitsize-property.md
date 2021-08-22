---
description: Spécifie la taille des unités d’accès vidéo, en octets. Cette propriété s’applique uniquement aux modes de contrôle VBR (variable bit rate).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Propriété AVEncVideoCodedVideoAccessUnitSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce45dbd232226aa5e0013cbead8e4ff2d8d82b5362d1d6a43cf45c2d030407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663164"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>Propriété AVEncVideoCodedVideoAccessUnitSize

Spécifie la taille des unités d’accès vidéo, en octets. Cette propriété s’applique uniquement aux modes de contrôle VBR (variable bit rate).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété est retournée sous la forme d’une plage de valeurs. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




