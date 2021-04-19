---
description: Spécifie si le DSP de capture vocale applique le délimitation du gain de microphone.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518140"
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

## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
