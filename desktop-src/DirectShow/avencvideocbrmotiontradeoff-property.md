---
description: Spécifie le compromis entre le mouvement et les images fixes. Cette propriété s’applique uniquement au mode de contrôle CBR (constant bit rate).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Propriété AVEncVideoCBRMotionTradeoff (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d3db1f310de6468b57d469fbf699919ab86429e7242344622ca498b9e59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057939"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>Propriété AVEncVideoCBRMotionTradeoff

Spécifie le compromis entre le mouvement et les images fixes. Cette propriété s’applique uniquement au mode de contrôle CBR (constant bit rate).

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoCBRMotionTradeoff**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est comprise dans la plage suivante.



| Valeur | Description               |
|-------|---------------------------|
| 0     | Optimiser pour les images fixes |
| 100   | Optimisez le mouvement.      |



 

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

 

 




