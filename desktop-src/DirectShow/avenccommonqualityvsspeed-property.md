---
description: Spécifie le compromis entre la qualité et la vitesse du codage. Cette propriété est valide dans tous les modes de contrôle de taux.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propriété AVEncCommonQualityVsSpeed (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9def8fc53a6cf88384a42870ef695294a0117ab3bfdd26ba69c95bd2b02a63b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540879"
---
# <a name="avenccommonqualityvsspeed-property"></a>Propriété AVEncCommonQualityVsSpeed

Spécifie le compromis entre la qualité et la vitesse du codage. Cette propriété est valide dans tous les modes de contrôle de taux.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonQualityVsSpeed**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est comprise dans la plage suivante.



| Valeur | Description                      |
|-------|----------------------------------|
| 0     | Une qualité inférieure, un encodage plus rapide.  |
| 100   | Qualité supérieure, encodage plus lent. |



 

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

 

 




