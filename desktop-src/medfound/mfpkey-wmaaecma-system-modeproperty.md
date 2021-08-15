---
description: Définit le mode de traitement pour le DSP de capture vocale.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722b3e502b783f98ef4871cfc6dd184389dfce7f7f942bde1827468e96f5fa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973268"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>\_Propriété du \_ mode système MFPKEY WMAAECMA \_

Définit le mode de traitement pour le DSP de capture vocale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
