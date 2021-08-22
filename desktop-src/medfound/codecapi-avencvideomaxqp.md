---
description: Spécifie le nombre maximal de QP pris en charge par l’encodeur.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: CODECAPI_AVEncVideoMaxQP, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d95f605dbb647ed96ec40e89870c761400a6d414cd354cb0197bb316bd3cf27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606319"
---
# <a name="codecapi_avencvideomaxqp-property"></a>CODECAPI \_ propriété AVEncVideoMaxQP

Spécifie le nombre maximal de QP pris en charge par l’encodeur.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoMaxQP**

## <a name="remarks"></a>Remarques

**Encodeurs H. 264/AVC :**

L’encodeur doit prendre en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Il s’agit d’une propriété statique, ce qui signifie qu’elle ne peut être définie que avant le démarrage de la session d’encodage.

La valeur par défaut est le nombre maximal de QP autorisé par la norme de codage correspondante. Par exemple, les encodeurs H. 264 doivent avoir une valeur par défaut de 51.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md)
</dt> </dl>

 

