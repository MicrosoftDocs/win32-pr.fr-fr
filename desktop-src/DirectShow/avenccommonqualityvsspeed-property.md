---
description: Spécifie le compromis entre la qualité et la vitesse du codage. Cette propriété est valide dans tous les modes de contrôle de taux.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Propriété AVEncCommonQualityVsSpeed (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111937"
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

 

 




