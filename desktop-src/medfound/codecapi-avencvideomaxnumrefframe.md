---
description: Spécifie le nombre maximal de frames de référence pris en charge par l’encodeur.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e11e7325628f0e7c1e6560d3fc734b34e8a032a3fbf3630aa1fb5959cec33a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606419"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>CODECAPI \_ propriété AVEncVideoMaxNumRefFrame

Spécifie le nombre maximal de frames de référence pris en charge par l’encodeur.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Remarques

Pour H. 264, cela est mappé aux images du paramètre de séquence Set **Max \_ num \_ Ref \_ frames** comme défini dans la spécification H. 264.

**Encodeurs H. 264/AVC :**

Les encodeurs peuvent utiliser moins de frames de référence pour respecter le niveau spécifié dans le flux binaire.

Les encodeurs prennent en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Il s’agit d’une propriété statique, ce qui signifie qu’elle ne peut être définie que avant le démarrage de la session d’encodage.

La valeur par défaut recommandée est 2.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

