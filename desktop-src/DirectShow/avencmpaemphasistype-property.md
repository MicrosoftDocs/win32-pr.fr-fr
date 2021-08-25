---
description: Spécifie le type de filtre de désaccentuation à utiliser lors du décodage. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Propriété AVEncMPAEmphasisType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3da73e2708acde7a5b388d229a3a82c50a2dff04c4f2873551a992fe738189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824229"
---
# <a name="avencmpaemphasistype-property"></a>Propriété AVEncMPAEmphasisType

Spécifie le type de filtre de désaccentuation à utiliser lors du décodage. Cette propriété s’applique aux encodeurs audio MPEG.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPAEmphasisType**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .

## <a name="remarks"></a>Remarques

Cette propriété définit les bits d’accentuation dans l’en-tête du frame.

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

 

