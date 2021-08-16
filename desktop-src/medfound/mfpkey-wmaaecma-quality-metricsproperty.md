---
description: Récupère les mesures de qualité sur l’annulation de l’écho acoustique (AEC) à partir du DSP de capture vocal.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: MFPKEY_WMAAECMA_QUALITY_METRICS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2186876279ee45e34444866c206a7729c0674c8dff1bc57c255ca205e911edae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689264"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>\_Propriété des \_ mesures de qualité MFPKEY WMAAECMA \_

Récupère les mesures de qualité sur l’annulation de l’écho acoustique (AEC) à partir du DSP de capture vocal.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

\_objet BLOB VT

## <a name="remarks"></a>Remarques

La valeur de cette propriété est une structure de [ \_ struct AecQualityMetrics](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) . Cette propriété est en lecture seule.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
