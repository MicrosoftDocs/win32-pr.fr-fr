---
description: Définit le mode de traitement pour le DSP de capture vocale.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520494"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>\_Propriété du \_ mode système MFPKEY WMAAECMA \_

Définit le mode de traitement pour le DSP de capture vocale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

La valeur de cette propriété est un membre de l’énumération du [ \_ \_ mode système AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .

La propriété doit avoir l’une des valeurs suivantes.



| Valeur | Description                                 |
|-------|---------------------------------------------|
| 0     | Mode d’annulation de l’écho audio (AEC) uniquement     |
| 2     | Mode de traitement du tableau de microphone (carte) uniquement |
| 4     | AEC et mode MAP                            |
| 5     | Ni AEC ni mode MAP                    |



 

Vous devez définir cette propriété avant d’utiliser le DSP de capture vocale. Une fois cette propriété définie, vous pouvez utiliser le DSP avec ses paramètres par défaut ou définir des propriétés supplémentaires.

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

 

 
