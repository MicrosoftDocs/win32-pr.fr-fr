---
description: Obtient ou définit la vitesse de décodage vidéo.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Propriété AVDecVideoFastDecodeMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112053"
---
# <a name="avdecvideofastdecodemode-property"></a>Propriété AVDecVideoFastDecodeMode

Obtient ou définit la vitesse de décodage vidéo.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété peut être comprise entre 0 et 32, où 0 indique un décodage normal et 32 le mode de décodage le plus rapide. Le comportement exact dépend de l’implémentation du décodeur. Tous les incréments compris entre 1 et 32 ne sont pas nécessairement définis comme un mode distinct.

L’énumération [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contient des modes prédéfinis pour cette propriété.

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

 

 




