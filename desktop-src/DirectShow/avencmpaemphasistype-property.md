---
description: Spécifie le type de filtre de désaccentuation à utiliser lors du décodage. Cette propriété s’applique aux encodeurs audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Propriété AVEncMPAEmphasisType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111814"
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

## <a name="remarks"></a>Notes

Cette propriété définit les bits d’accentuation dans l’en-tête du frame.

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

 

