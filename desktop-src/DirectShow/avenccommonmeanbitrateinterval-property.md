---
description: Spécifie l’intervalle de temps pendant lequel la vitesse de transmission moyenne s’applique. Cette propriété est utilisée conjointement avec la propriété AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Propriété AVEncCommonMeanBitRateInterval (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111961"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>Propriété AVEncCommonMeanBitRateInterval

Spécifie l’intervalle de temps pendant lequel la vitesse de transmission moyenne s’applique. Cette propriété est utilisée conjointement avec la propriété [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété a une plage de valeurs linéaire. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Notes

Pour l’encodage VBR (variable bit rate) à deux passes, la valeur zéro indique que l’intervalle de temps correspond à la durée totale du contenu. Pour l’encodage CBR (Single-passe constant bit rate), la valeur zéro indique que l’encodeur sélectionne l’intervalle (en général 0,5 secondes).

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

 

 




