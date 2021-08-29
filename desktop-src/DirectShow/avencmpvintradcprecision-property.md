---
description: Spécifie la précision des coefficients DC, en bits. Cette propriété s’applique aux encodeurs vidéo MPEG.
ms.assetid: 2b4d11c1-767c-4466-8291-7959d841ae65
title: Propriété AVEncMPVIntraDCPrecision (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e50d4a6b222d9860a16216a1395b9f5a2b10d23e6242315a61e8224d37810c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276129"
---
# <a name="avencmpvintradcprecision-property"></a>Propriété AVEncMPVIntraDCPrecision

Spécifie la précision des coefficients DC, en bits. Cette propriété s’applique aux encodeurs vidéo MPEG.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncMPVIntraDCPrecision**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Remarques

La plage habituelle de cette propriété est comprise entre 8 et 11 bits. Si la valeur est égale à zéro, l’encodeur sélectionne la précision.

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

 

 




