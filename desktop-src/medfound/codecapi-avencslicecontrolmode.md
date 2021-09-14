---
description: Spécifie le mode de contrôle de la section. Les valeurs valides sont 0, 1 et 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236309"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>CODECAPI \_ propriété AVEncSliceControlMode

Spécifie le mode de contrôle de la section. Les valeurs valides sont 0, 1 et 2.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valeur de la propriété

Valeurs du mode de contrôle Slice :



| Valeur                                                                        | Signification                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Si cette valeur est définie sur 0, cela signifie que la propriété [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) spécifie la taille de la tranche en unités de blocs macros par tranche.<br/>     |
| <dl> <dt>1</dt> </dl> | Si la valeur 1 est définie, la propriété [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) spécifie la taille de la tranche en unités de bits par tranche.<br/>            |
| <dl> <dt>2</dt> </dl> | Si cette valeur est définie sur 2, la propriété [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) spécifie la taille de la tranche en unités de lignes bloc macro par tranche.<br/> |



 

L’encodeur retourne les valeurs qu’il prend en charge.

## <a name="remarks"></a>Notes

**Encodeurs H. 264/AVC :**

Il est recommandé que l’encodeur prenne en charge [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)et [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Si [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) n’est pas appelé pour CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) pour CODECAPI \_ AVEncSliceControlMode peut retourner **VFW \_ E \_ CODECAPI \_ aucune \_ \_ valeur actuelle**. [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) peut retourner **VFW \_ E \_ CODECAPI \_ pas de \_ valeur par défaut** pour CODECAPI \_ AVEncSliceControlMode.

La valeur par défaut recommandée est 2 (taille en Mo par tranche).

Il s’agit d’une API statique, ce qui signifie que l’application a gagné la modification pendant que l’encodeur est en cours d’exécution.

## <a name="examples"></a>Exemples


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

