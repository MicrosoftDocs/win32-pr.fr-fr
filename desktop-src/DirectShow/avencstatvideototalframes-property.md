---
description: Retourne le nombre de trames vidéo reçues par l’encodeur.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Propriété AVEncStatVideoTotalFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111670"
---
# <a name="avencstatvideototalframes-property"></a>Propriété AVEncStatVideoTotalFrames

Retourne le nombre de trames vidéo reçues par l’encodeur.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Notes

Cette propriété est disponible une fois l’encodage terminé.

La valeur de cette propriété est le nombre total de trames envoyées à l’encodeur, y compris les frames qui ont été supprimés. Pour obtenir le nombre de frames encodés, lisez la propriété [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .

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

 

 




