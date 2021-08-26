---
description: Spécifie si le DSP de capture vocale applique le délimitation du gain de microphone.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d00e906ec953e2fd00d9c288336c322c2d0dc07ea1c2d74a014ab78ae21acd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113149"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>Propriété de MFPKEY \_ WMAAECMA \_ MIC \_ gain \_

Spécifie si le DSP de capture vocale applique le délimitation du gain de microphone.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ true

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

Le gain de gain de microphone garantit que le microphone a le niveau de gain correct. Si le gain est trop élevé, le signal capturé peut être saturé et sera coupé. Le découpage est un effet non linéaire qui entraîne l’échec de l’algorithme d’annulation de l’écho acoustique (AEC). Si le gain est trop faible, le rapport signal-bruit est faible, ce qui peut également entraîner l’échec ou l’inefficacité de l’algorithme AEC.

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description                       |
|----------------|-----------------------------------|
| VARIANTE \_ true  | Activez le délimitation du gain de microphone.  |
| VARIANTE \_ false | Désactive le délimitation du gain de microphone. |



 

La valeur par défaut de cette propriété est \_ true (activé).

Le délimitation du gain de microphone s’applique uniquement lorsque le DSP fonctionne en mode Source. En mode filtre, l’application doit s’assurer que le microphone a le niveau de gain correct.

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

 

 
